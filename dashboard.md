<html lang="en">

<head>
    <meta charset="utf-8">
    <!--  This file has been downloaded from bootdey.com    @bootdey on twitter -->
    <!--  All snippets are MIT license http://bootdey.com/license -->
    <title>EIS Dashboard</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link href="http://netdna.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" rel="stylesheet">
    <style type="text/css">
        body {
            background: #edf1f5;
            margin-top: 20px;
        }

        .card {
            position: relative;
            display: flex;
            flex-direction: column;
            min-width: 0;
            word-wrap: break-word;
            background-color: #fff;
            background-clip: border-box;
            border: 0 solid transparent;
            border-radius: 0;
        }

        .card {
            margin-bottom: 30px;
        }

        .card-body {
            flex: 1 1 auto;
            padding: 1.57rem;
        }

        .note-has-grid .nav-link {
            padding: .5rem
        }

        .note-has-grid .single-note-item .card {
            border-radius: 10px
        }

        .note-has-grid .single-note-item .favourite-note {
            cursor: pointer
        }

        .note-has-grid .single-note-item .side-stick {
            position: absolute;
            width: 3px;
            height: 35px;
            left: 0;
            background-color: rgba(82, 95, 127, .5)
        }

        .note-has-grid .single-note-item .category-dropdown.dropdown-toggle:after {
            display: none
        }

        .note-has-grid .single-note-item .category [class*=category-] {
            height: 15px;
            width: 15px;
            display: none
        }

        .note-has-grid .single-note-item .category [class*=category-]::after {
            content: "\f0d7";
            font: normal normal normal 14px/1 FontAwesome;
            font-size: 12px;
            color: #fff;
            position: absolute
        }

        .note-has-grid .single-note-item .category .category-business {
            background-color: rgba(44, 208, 126, .5);
            border: 2px solid #2cd07e
        }

        .note-has-grid .single-note-item .category .category-social {
            background-color: rgba(44, 171, 227, .5);
            border: 2px solid #2cabe3
        }

        .note-has-grid .single-note-item .category .category-important {
            background-color: rgba(255, 80, 80, .5);
            border: 2px solid #ff5050
        }

        .note-has-grid .single-note-item.all-category .point {
            color: rgba(82, 95, 127, .5)
        }

        .note-has-grid .single-note-item.note-business .point {
            color: rgba(44, 208, 126, .5)
        }

        .note-has-grid .single-note-item.note-business .side-stick {
            background-color: rgba(44, 208, 126, .5)
        }

        .note-has-grid .single-note-item.note-business .category .category-business {
            display: inline-block
        }

        .note-has-grid .single-note-item.note-favourite .favourite-note {
            color: #ffc107
        }

        .note-has-grid .single-note-item.note-social .point {
            color: rgba(44, 171, 227, .5)
        }

        .note-has-grid .single-note-item.note-social .side-stick {
            background-color: rgba(44, 171, 227, .5)
        }

        .note-has-grid .single-note-item.note-social .category .category-social {
            display: inline-block
        }

        .note-has-grid .single-note-item.note-important .point {
            color: rgba(255, 80, 80, .5)
        }

        .note-has-grid .single-note-item.note-important .side-stick {
            background-color: rgba(255, 80, 80, .5)
        }

        .note-has-grid .single-note-item.note-important .category .category-important {
            display: inline-block
        }

        .note-has-grid .single-note-item.all-category .more-options,
        .note-has-grid .single-note-item.all-category.note-favourite .more-options {
            display: block
        }

        .note-has-grid .single-note-item.all-category.note-business .more-options,
        .note-has-grid .single-note-item.all-category.note-favourite.note-business .more-options,
        .note-has-grid .single-note-item.all-category.note-favourite.note-important .more-options,
        .note-has-grid .single-note-item.all-category.note-favourite.note-social .more-options,
        .note-has-grid .single-note-item.all-category.note-important .more-options,
        .note-has-grid .single-note-item.all-category.note-social .more-options {
            display: none
        }

        @media (max-width:767.98px) {
            .note-has-grid .single-note-item {
                max-width: 100%
            }
        }

        @media (max-width:991.98px) {
            .note-has-grid .single-note-item {
                max-width: 216px
            }
        }
    </style>

    <!-- The core Firebase JS SDK is always required and must be listed first -->
    <script src="https://www.gstatic.com/firebasejs/8.6.2/firebase-app.js"></script>

    <!-- TODO: Add SDKs for Firebase products that you want to use
   https://firebase.google.com/docs/web/setup#available-libraries -->
    <script src="https://www.gstatic.com/firebasejs/8.6.2/firebase-firestore.js"></script>
    <script src="https://www.gstatic.com/firebasejs/8.6.2/firebase-database.js"></script>
    <script src="https://www.gstatic.com/firebasejs/8.6.2/firebase-analytics.js"></script>

    <script>

        var variation = Math.floor(Math.random() * 2) + 1

        // Your web app's Firebase configuration
        // For Firebase JS SDK v7.20.0 and later, measurementId is optional
        var firebaseConfig = {
            apiKey: "AIzaSyBeZIZbmexkwdyUtlaUS4IxZz_LJsYai1Y",
            authDomain: "moviestar-abtesting.firebaseapp.com",
            databaseURL: "https://moviestar-abtesting-default-rtdb.firebaseio.com",
            projectId: "moviestar-abtesting",
            storageBucket: "moviestar-abtesting.appspot.com",
            messagingSenderId: "1045023498731",
            appId: "1:1045023498731:web:244937af969bfea91639ae",
            measurementId: "G-RNGV3KD9YD"
        };
        // Initialize Firebase
        firebase.initializeApp(firebaseConfig);

        console.log("firebase initialised")

        let rtdb = firebase.database();
        firebase.analytics();

        function loadData() {
            rtdb.ref().child('values').child('0').child('dashboardValues').on('value', (snapshot) => {
                if (snapshot.exists()) {
                    let rawData = snapshot.val(); // "72 168 240 1 -8.8 2021-05-28 12:31:46 (GMT) (Non-significant)"
                    let dataArray = rawData.split(" ");
                    console.log(dataArray)

                    let aLength = dataArray[0];
                    let bLength = dataArray[1];
                    let totalLength = dataArray[2];
                    let pValue = dataArray[3];
                    let zValue = dataArray[4];
                    let date = dataArray[5];
                    let time = dataArray[6] + " " + dataArray[7];
                    let significance = dataArray[8];

                    let noInterimAnalysis = Math.floor((310 - totalLength)/22);

                    let experimentDate = Date.parse(date);
                    let experimentDateText = new Intl.DateTimeFormat('en', { dateStyle: 'medium' }).format(experimentDate)

                    let tomorrowDate = new Date()
                    tomorrowDate.setDate(tomorrowDate.getDate() + 1)
                    let tomorrowDateText = new Intl.DateTimeFormat('en', { dateStyle: 'medium' }).format(tomorrowDate)

                    Array.from(document.getElementsByClassName('note-date')).forEach((element) => {
                        element.innerHTML = experimentDateText
                    })

                    document.getElementById('latest_analysis_text').innerHTML = "The latest analysis was conducted on <span style='color:cornflowerblue'>" + experimentDateText + "</span>" + " at <span style='color:cornflowerblue'>" + time + "</span>, after <span style='color:cornflowerblue'>" + totalLength + "</span> subjects entered the experiment (" + aLength + " in group A and " + bLength + " in group B)."
                    
                    document.getElementById('key_values_text').innerHTML = "<span style='color:cornflowerblue'>Z = " + zValue + "</span>, <span style='color:red'>p-value = " + pValue + "</span> " + significance

                    document.getElementById('interim_analysis_text').innerHTML = "<span style='color:cornflowerblue'>" + noInterimAnalysis + " interim analysis pending</span> (total subjects = 310 for power = 80%)"

                    document.getElementById('estimated_time_date').innerHTML = "Estimated time for <span style='color:cornflowerblue'>next analysis: " + tomorrowDateText + " at 13:47</span>."

                    document.getElementById('estimated_time_duration').innerHTML = "Estimated time for <span style='color:cornflowerblue'>completion: " + noInterimAnalysis + " days</span>."
                } else {

                }
            })
        }
    </script>
</head>

<body onload="loadData()">
    <link href="https://maxcdn.bootstrapcdn.com/font-awesome/4.3.0/css/font-awesome.min.css" rel="stylesheet">
    <div class="page-content container note-has-grid">
        <div class="tab-content bg-transparent">
            <div id="note-full-container" class="note-has-grid row">
                <div class="col-md-4 single-note-item all-category" style="">
                    <div class="card card-body">
                        <span class="side-stick"></span>
                        <h5 class="note-title text-truncate w-75 mb-0" data-noteheading="Latest Analysis">Latest
                            Analysis <i class="point fa fa-circle ml-1 font-10"></i></h5>
                        <p class="note-date font-12 text-muted">25 May 2021</p>
                        <div class="note-content">
                            <p id="latest_analysis_text" class="note-inner-content text-muted"
                                data-notecontent="Latest Analysis Content">The
                                latest analysis was conducted on May 25 at 18:54, after 176 subjects entered the
                                experiment (88 in group A and 88 in group B).</p>
                        </div>
                    </div>
                </div>
                <div class="col-md-4 single-note-item all-category note-important">
                    <div class="card card-body">
                        <span class="side-stick"></span>
                        <h5 class="note-title text-truncate w-75 mb-0" data-noteheading="Key Values">Key Values <i
                                class="point fa fa-circle ml-1 font-10"></i></h5>
                        <p class="note-date font-12 text-muted">25 May 2021</p>
                        <div class="note-content">
                            <p id="key_values_text" class="note-inner-content text-muted"
                                data-notecontent="Key Values content">Z = 1.83,
                                <span style='color:red'>p-value = 0.28</span> (non-significant)
                            </p>
                        </div>
                    </div>
                </div>
                <div class="col-md-4 single-note-item all-category note-social" style="">
                    <div class="card card-body">
                        <span class="side-stick"></span>
                        <h5 class="note-title text-truncate w-75 mb-0" data-noteheading="Interim Analysis">Interim
                            Analysis <i class="point fa fa-circle ml-1 font-10"></i></h5>
                        <p class="note-date font-12 text-muted">25 May 2021</p>
                        <div class="note-content">
                            <p id="interim_analysis_text" class="note-inner-content text-muted"
                                data-notecontent="Interim Analysis content"><span style="color:cornflowerblue">4 interim
                                    analysis pending</span> (total subjects = 310
                                for power = 80%)</p>
                        </div>
                    </div>
                </div>
                <div class="col-md-4 single-note-item all-category note-business" style="">
                    <div class="card card-body">
                        <span class="side-stick"></span>
                        <h5 class="note-title text-truncate w-75 mb-0" data-noteheading="Estimated Time">Estimated Time
                            <i class="point fa fa-circle ml-1 font-10"></i>
                        </h5>
                        <p class="note-date font-12 text-muted">25 May 2021</p>
                        <div class="note-content">
                            <p id="estimated_time_date" class="note-inner-content text-muted"
                                data-notecontent="Estimated Time content">Estimated
                                time for <span style="color:cornflowerblue">next analysis: May 27th at 13:47</span>.</p>
                            <p id="estimated_time_duration" class="note-inner-content text-muted"
                                data-notecontent="Estimated Time content">Estimated
                                time for <span style="color:cornflowerblue">completion: 5 days</span>.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script src="http://code.jquery.com/jquery-1.10.2.min.js"></script>
    <script src="http://netdna.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js"></script>
</body>

</html>
