---
title: movistar
id: movistar_v2
layout: none
nav-menu: false
show_tile: false
---

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>movistar</title>

  <link rel="stylesheet" href="style.css">
  <link rel="stylesheet" href="mediaquery.css">
  <link rel="stylesheet" href="https://maxst.icons8.com/vue-static/landings/line-awesome/line-awesome/1.3.0/css/line-awesome.min.css">
  <script src="https://kit.fontawesome.com/bc3a1796c2.js" crossorigin="anonymous"></script>
  <link rel="shortcut icon" href="https://image.flaticon.com/icons/png/512/870/870910.ico'/> 
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.css" />
</head>
<style>
  @import url("https://fonts.googleapis.com/css?family=IBM+Plex+Sans&display=swap");
  @import url("https://fonts.googleapis.com/css?family=Martel+Sans&display=swap");
  @import url("https://fonts.googleapis.com/css?family=Roboto&display=swap");

  body {
    margin: 0;
    padding: 0;
    flex-wrap: wrap;
    display: flex;
    font-family: "Roboto", sans-serif;

    background-color: rgba(8, 8, 8, 0.89);
  }

  .navbar {
    display: flex;
    flex-direction: row;
    position: relative;
    align-items: center;
    width: 100%;
    height: 50px;
    min-height: 100px;
    align-items: center;
    justify-content: space-between;
    background-color: transparent;
    align-self: center;
  }

  .navbar li {
    margin: 0 50px;
    list-style-type: none;
    display: flex;
    flex-direction: row;
  }

  .navbar li:nth-child(2) {
    margin-right: -650px;
  }

  .logo img {
    width: 180px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    align-self: center;
  }

  .logo {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    align-self: center;
  }

  .buttons {
    background-color: #e50914;
    padding: 7px 17px;
    color: white;
    display: flex;
    flex-direction: row;
    border-radius: 3px;
    cursor: pointer;
  }

  .secondary-buttons {
    color: white;
    cursor: pointer;
    position: absolute;
    right: 150px;
    padding: 7px 17px;
    border-radius: 3px;
    border: 1px solid white;
  }

  .main {
    width: 100%;
    margin-top: -100px;
    background-size: cover;
    align-items: center;
    overflow-x: hidden;
    justify-content: center;
    display: flex;
    background-position: center;
    min-height: 710px;
    background-image: linear-gradient(rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.8)),
      url(https://images.unsplash.com/photo-1536440136628-849c177e76a1?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1250&q=80);
  }

  .area {
    color: white;
    display: inline-flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    margin-top: 70px;
  }

  .area h1 {
    font-size: 60px;
    word-spacing: 15px;
    line-height: 75px;
  }

  .area h3 {
    margin-top: -30px;
    font-size: 27px;
    font-weight: normal;
  }

  .search {
    width: 150%;
    background-color: none;
    min-height: 80px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    text-align: left;
    margin-top: 10px;
  }

  .box {
    width: 100%;
    min-height: 65px;
  }

  .try {
    display: inline-flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    background-color: #e50914;
    min-height: 70px;
    width: 70%;
    font-size: 30px;
    text-transform: uppercase;
    cursor: pointer;
  }

  .area h4 {
    margin-top: 10px;
    font-weight: normal;
  }
  .container1 {
    width: 100%;
    min-height: 460px;
    background-color: black;
    margin-top: 10px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-evenly;
    text-align: left;
  }

  .container1 img {
    display: flex;
    justify-content: center;
    flex-direction: row;
    object-fit: contain;
    object-position: center;
    align-self: center;

    max-width: 100%;
    height: 350px;
  }

  .container1 .image {
    display: flex;
    justify-content: center;
    flex-direction: row;
    align-items: center;
    align-self: center;
    object-fit: contain;
  }

  .text {
    color: white;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    align-self: center;
    align-content: center;
  }
  .text p {
    font-size: 1.5rem;
    margin-top: 5px;
  }

  .text h1 {
    font-size: 3.125rem;
  }

  .question {
    width: 100%;
    min-height: 950px;
    background-color: #000;
    margin-top: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-end;
    text-align: center;
  }

  .question h1 {
    text-align: center;
    color: white;
    margin-bottom: 50px;
    text-align: center;
    font-size: 40px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .quest {
    width: 51%;
    min-height: 75px;
    background-color: #303030;
    color: white;
    align-items: center;
    justify-content: space-between;
    display: flex;
    text-align: left;
    flex-direction: row;
    margin: 5px 0;
  }

  .quest .textbox {
    display: flex;
    text-align: left;

    flex-direction: row;
    align-items: center;
    justify-content: center;
    justify-items: center;
    align-self: center;
    font-size: 25px;
    margin: 0 30px;
    word-spacing: 5px;
    text-align: left;
  }

  .quest i {
    margin: 0 30px;
    font-size: 40px;
    color: rgb(255, 255, 255);
  }

  .quest:focus {
    background-color: red;
  }

  .search1 {
    width: 50%;
    background-color: none;
    min-height: 80px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    text-align: left;
    margin-top: 10px;
  }

  .box1 {
    width: 100%;
    min-height: 65px;
  }

  .try1 {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    background-color: #e50914;
    min-height: 70px;
    width: 70%;
    color: white;
    font-size: 30px;
    margin: 50px 0;
    text-transform: uppercase;
  }

  .question h4 {
    color: white;
    margin-top: -20px;
    padding-bottom: 40px;
  }

  .footer {
    display: flex;
    flex-direction: column;
    width: 100%;
    min-height: 375px;
    background-color: black;
    margin-top: 10px;
    flex-wrap: wrap;
    align-items:center;
    justify-content:space-around;

  }

  .footercon {
    display: flex;
    flex-direction: row;
    width: 100%;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    min-height: 50px;
    background-color: transparent;
  }

  .footer .flex1 {
    color:#999;;
    justify-content:space-around;
    align-items:flex-start;
    display: flex;
    flex-direction:row;
    flex-wrap:wrap;
    width:100%;
    font-size: 17px;
    min-height: 30px;

  }

  .footer .flex1 h5 {
    align-self:flex-start;
  }

  .list1 {
    color: white;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    align-items: flex-start;
    justify-items: flex-start;
    align-self: center;
    justify-content: center;
    min-height:50px;
    font-size: 13px;
    padding: 0px 70px;
    text-align: left;
  }

  .list1 li {
    font-size: 13px;
    margin: 7px -10px;
    list-style-type: none;
    text-align: left;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    align-items: flex-start;
    justify-items: center;
    align-self: flex-start;
    justify-content: center;
  }

  .list1 li a {
    color: #999;
    text-decoration: none;
    font-size: 14px;
  }

  li a {
    font-size: 13px;
    text-align: center;
    color: #999;
  }


  .footertxt {
    color:white;
    display:flex;
    flex-direction:row;
    align-items:flex-end;
    justify-content: flex-end;
  }

  .end {
    width:100%;
    min-height:50px;
  background-color: black;
  justify-content:space-around;
  align-items:flex-start;
  display: flex;
  flex-direction:row;
  flex-wrap:wrap;
  color:#999;
  margin-top:-60px;
  }

  .end h2 {
    display:flex;
    flex-direction: row;
  font-size:16px;
  }

  @media (min-width: 250px) and (max-width: 980px) {
    body {
      display: flex;
      flex-direction: column;
      flex-wrap: wrap;
    }
    .container1 {
      display: flex;
      flex-direction: column;
      justify-content: space-evenly;
      align-items: center;
      align-self: center;
    }

    .area h1 {
      font-size: 40px;
      line-height:60px;
    }

    .area h3 {
      margin-top: 10px;
    }

    .container1 img {
      width: 60%;
    }
    .navbar {
      display: flex;
      flex-direction: column;
      background-color: black;
      align-items: center;
      justify-content: center;
      padding: 0;
      min-height: 250px;
      margin-bottom: 30px;

    }



    .search {
      display: flex;
      flex-direction: column;
      margin: 30px;
      width: 50%;
      margin: 0 10px;
    }

    .box {
      width: 100%;
      margin-bottom: 20px;
      margin:30px;
    }

    .try {
      width: 200px;
      margin: 0 10px;
      font-size:17px;
      min-height:50px;
    }

    .search1 {
      display: flex;
      flex-direction: column;
      margin: 30px;
      width: 50%;
      margin: 0 10px;
      margin-bottom: 40px;
    }

  h4 {
    color:white;
  }

    .box1 {
      width: 100%;
      margin-bottom: 20px;
      margin:30px;
    }

    .try1 {
      width: 200px;
      margin: 0 10px;
      font-size:17px;
      min-height:50px;
    }
    .text {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      align-self: center;
      text-align: center;
      margin-left: 10px;
      margin-right: 10px;
    }

    .text h1 {
      font-size: 2rem;
      margin-left: 10px;
      margin-right: 10px;
    }

    .text p {
      font-size: 1.2rem;
      margin-left: 10px;
      margin-right: 10px;
    }

    .quest .textbox {
      font-size: 20px;
      margin-left: 10px;
      margin-right: 10px;
    }

    .quest {
      width: 80%;
      min-height: 75px;
      margin-left: 10px;
      margin-right: 10px;
    }
  }
</style>
<body>

  <div class="navbar">
    <li class="logo">
      <svg
         xmlns:dc="http://purl.org/dc/elements/1.1/"
         xmlns:cc="http://creativecommons.org/ns#"
         xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
         xmlns:svg="http://www.w3.org/2000/svg"
         xmlns="http://www.w3.org/2000/svg"
         xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
         xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
         width="200pt"
         height="118pt"
         viewBox="0 0 604 118"
         version="1.1"
         id="svg26"
         sodipodi:docname="Logo_Movistar.svg"
         inkscape:version="0.92.2 (5c3e80d, 2017-08-06)">
        <metadata
           id="metadata32">
          <rdf:RDF>
            <cc:Work
               rdf:about="">
              <dc:format>image/svg+xml</dc:format>
              <dc:type
                 rdf:resource="http://purl.org/dc/dcmitype/StillImage" />
            </cc:Work>
          </rdf:RDF>
        </metadata>
        <defs
           id="defs30" />
        <sodipodi:namedview
           pagecolor="#ffffff"
           bordercolor="#666666"
           borderopacity="1"
           objecttolerance="10"
           gridtolerance="10"
           guidetolerance="10"
           inkscape:pageopacity="0"
           inkscape:pageshadow="2"
           inkscape:window-width="1920"
           inkscape:window-height="1028"
           id="namedview28"
           showgrid="false"
           inkscape:zoom="1.2257298"
           inkscape:cx="668.52459"
           inkscape:cy="-75.594385"
           inkscape:window-x="-8"
           inkscape:window-y="-8"
           inkscape:window-maximized="1"
           inkscape:current-layer="svg26" />
        <g
           id="#00abe1ff">
          <path
             d="m 125.21,1.18 c 4.94,-0.77 10.42,-0.88 14.81,1.91 6.34,3.77 9.96,10.6 12.46,17.3 7.03,19.32 7.7,40.45 4.75,60.64 -0.66,5.17 -2.64,11.01 -7.71,13.36 -3,1.01 -6.84,0.74 -8.92,-1.92 -3.36,-4.06 -2.3,-9.66 -2.02,-14.49 1.09,-7.63 1.51,-15.37 1.16,-23.06 -0.03,-3.51 -1.21,-7.31 -4.22,-9.38 -2.54,-1.92 -6.21,-1.55 -8.73,0.21 -4.27,2.77 -7.07,7.23 -9.36,11.67 -5.62,11.57 -8.73,24.12 -12.92,36.23 -2.1,5.63 -5.49,10.99 -10.52,14.42 -6.03,4.25 -13.69,5.37 -20.91,5.11 -9.22,-0.44 -17.52,-6.23 -22.36,-13.89 -6.03,-9.75 -11.4,-19.9 -17.29,-29.73 -1.87,-2.86 -4.39,-6.52 -8.29,-6.1 -4.1,0.38 -5.65,4.97 -5.52,8.51 0.29,12.13 6.16,23.18 8.25,34.99 0.73,3.64 -0.31,8.21 -3.98,9.86 -2.24,0.31 -4.59,0.59 -6.81,0.01 -3.26,-1.24 -4.95,-4.61 -6.41,-7.54 C 5.58,97.09 2.41,84.14 0.78,71.05 1.01,64.34 0.38,57.54 1.8,50.92 3.74,40.12 6.71,28.69 14.72,20.71 c 6.9,-6.99 18.78,-9.07 27.15,-3.56 8.12,5.63 13.14,14.37 18.47,22.45 3.91,6.22 7.56,13.54 14.74,16.53 4.95,2.41 11.3,0.93 14.94,-3.12 2.61,-2.69 3.9,-6.28 5.28,-9.69 2.93,-7.34 5.85,-14.67 9.06,-21.89 3.65,-9.25 10.84,-17.85 20.85,-20.25 z"
             id="path7"
             inkscape:connector-curvature="0"
             style="opacity:1;fill:#00abe1" />
          <path
             d="m 484.27,24.47 c 3.74,-0.29 7.5,-0.12 11.24,0.01 0.28,3.76 -0.23,7.55 0.34,11.29 3.83,-0.13 7.68,-0.24 11.51,0.06 0.1,3.33 0.46,6.7 -0.25,9.99 -3.82,-0.07 -7.63,-0.05 -11.44,0.02 -0.18,8.04 -0.04,16.1 -0.09,24.14 0.04,3.41 -0.01,7.33 2.59,9.91 2.58,2.47 6.46,2.09 9.76,2.39 0.47,3.45 0.51,6.97 -0.13,10.4 -6.27,0.07 -13.17,-0.05 -18.29,-4.19 -4.6,-3.66 -5.91,-9.83 -6.06,-15.42 -0.09,-15 0.06,-30.01 -0.06,-45.01 0.26,-1.1 -0.61,-3.2 0.88,-3.59 z"
             id="path9"
             inkscape:connector-curvature="0"
             style="opacity:1;fill:#00abe1" />
          <path
             d="m 201.02,40.03 c 5.67,-5.09 13.75,-5.72 21.02,-5.45 5.92,-0.02 11.86,1.61 16.53,5.31 5.23,-5.43 13.34,-5.45 20.34,-5.31 6.39,0 13.22,1.9 17.53,6.88 3.18,3.73 3.77,8.83 3.87,13.55 0.04,9.97 0,19.94 0.02,29.92 -0.02,2.59 0.28,5.25 -0.54,7.75 -3.72,-0.16 -7.44,0.17 -11.14,-0.19 l -0.39,-0.56 c -0.4,-12.99 0.36,-26.02 -0.42,-39 0.07,-4.17 -3.79,-7.23 -7.71,-7.51 -4.47,-0.28 -9.67,-0.82 -13.32,2.35 -2.72,2.24 -2.4,6.07 -2.57,9.24 -0.12,10.32 -0.07,20.65 -0.04,30.97 -0.25,1.45 0.47,3.52 -0.78,4.58 -3.79,0.13 -7.63,0.27 -11.41,-0.17 0,-13.17 0.31,-26.34 -0.32,-39.5 -0.02,-4.44 -4.45,-7.42 -8.56,-7.54 -3.77,-0.19 -7.87,-0.49 -11.27,1.45 -2.2,1.22 -3.53,3.64 -3.59,6.13 -0.86,13.22 -0.05,26.48 -0.55,39.71 -3.83,0 -7.66,-0.03 -11.48,0.03 -0.38,-1.85 -0.55,-3.73 -0.48,-5.61 0.13,-11.03 -0.1,-22.06 0.11,-33.08 0.06,-5.03 1.2,-10.49 5.15,-13.95 z"
             id="path11"
             inkscape:connector-curvature="0"
             style="opacity:1;fill:#00abe1" />
          <path
             d="m 305.49,35.72 c 8.8,-1.74 18.56,-2.1 26.83,1.91 7.78,3.99 9.74,13.49 10.06,21.47 0.12,8.76 0.65,18.34 -4.15,26.09 -4.46,6.99 -13.55,8.6 -21.23,8.42 -7.36,0.2 -15.73,-0.85 -20.89,-6.67 -5.58,-6.96 -5.53,-16.48 -5.54,-24.95 0.22,-6.93 0.84,-14.51 5.19,-20.22 2.4,-3.09 6.01,-5.02 9.73,-6.05 m 5.01,9.93 c -3.48,0.74 -6.03,3.79 -6.71,7.19 -1.25,7.36 -1.25,14.93 -0.04,22.29 0.69,2.9 2.34,5.93 5.34,6.91 4.48,1.48 9.42,1.4 13.98,0.3 3.32,-0.68 5.43,-3.76 6.19,-6.87 1.36,-7.56 1.3,-15.33 -0.01,-22.89 -0.89,-3.49 -3.65,-6.56 -7.34,-7.07 -3.78,-0.45 -7.66,-0.52 -11.41,0.14 z"
             id="path13"
             inkscape:connector-curvature="0"
             style="opacity:1;fill:#00abe1" />
          <path
             d="m 440.35,37.4 c 8.19,-4.09 17.81,-2.99 26.55,-1.68 1.13,0.44 3.39,0.04 3.61,1.67 0.14,2.75 0.11,5.52 0.05,8.28 -0.35,0.14 -1.05,0.43 -1.4,0.57 -6.33,-1.1 -12.84,-2.23 -19.26,-1.21 -2.52,0.43 -5.73,1.94 -5.69,4.92 -0.57,2.54 1.64,4.31 3.64,5.29 7.04,3.23 15.02,4.73 21.24,9.57 5.21,3.97 5.73,11.42 4.07,17.28 -2.63,7.44 -10.76,10.97 -18.14,11.37 -7.02,0.32 -14.39,0.13 -20.95,-2.59 -1.25,-3.08 -0.46,-6.7 -0.35,-9.98 7.96,1.92 16.51,4.02 24.56,1.41 4.12,-1.09 5.63,-7.08 2.06,-9.66 -7.14,-4.38 -16.03,-5.23 -22.83,-10.26 -7.85,-6.33 -6.12,-20.47 2.84,-24.98 z"
             id="path15"
             inkscape:connector-curvature="0"
             style="opacity:1;fill:#00abe1" />
          <path
             d="m 521.66,38.01 c -0.36,-1.45 1.23,-2.29 2.42,-2.35 8.23,-1.11 16.69,-1.79 24.88,0.01 5.24,1.33 10.37,4.54 12.63,9.64 2.86,6.17 1.77,13.12 1.98,19.69 -0.14,6.48 0.73,13.38 -2.15,19.43 -2.78,5.8 -9.52,8.21 -15.49,8.98 -7.45,0.46 -15.44,0.55 -22.15,-3.19 -11.04,-6.18 -10.61,-24.98 0.67,-30.69 8.32,-4.39 18.07,-2.96 27.01,-1.94 0.24,-4.2 -0.43,-9.44 -4.8,-11.33 -8.03,-3.11 -16.69,-0.51 -24.97,-0.58 -0.02,-2.56 -0.12,-5.12 -0.03,-7.67 m 8.09,42.22 c 3.34,3.62 8.73,3.35 13.24,3.19 3.05,-0.11 6.57,-1.39 7.8,-4.43 1.04,-3.64 0.52,-7.49 0.69,-11.23 -5.69,-1.48 -11.79,-1.84 -17.57,-0.71 -5.76,1.05 -8.01,8.99 -4.16,13.18 z"
             id="path17"
             inkscape:connector-curvature="0"
             style="opacity:1;fill:#00abe1" />
          <path
             d="m 578.56,40.41 c 6.33,-6.38 16.11,-6.22 24.45,-5.63 0.24,3.38 0.17,6.77 -0.06,10.15 -4.61,0.79 -9.97,-0.92 -13.96,2.14 -2.46,1.79 -2.72,5.1 -2.8,7.88 -0.23,12.48 0,24.97 -0.12,37.45 -3.91,0.51 -7.85,0.09 -11.77,0.31 -0.96,-10.16 -0.15,-20.44 -0.42,-30.65 0.19,-7.33 -0.97,-15.93 4.68,-21.65 z"
             id="path19"
             inkscape:connector-curvature="0"
             style="opacity:1;fill:#00abe1" />
          <path
             d="m 349.03,35.79 c 4.22,-0.07 8.51,-0.54 12.68,0.31 1.01,15.47 5.39,30.68 12.23,44.56 1.17,-1.51 1.9,-3.29 2.61,-5.05 5.36,-12.52 9.07,-25.88 9.81,-39.53 4.15,-0.8 8.41,-0.39 12.61,-0.26 -0.56,19.68 -8.82,38.11 -17.68,55.35 -0.62,1.86 -2.81,1.39 -4.29,1.49 -3.1,-0.1 -6.22,0.21 -9.29,-0.21 -0.25,-0.31 -0.75,-0.93 -1,-1.24 -9.26,-17.1 -17.15,-35.69 -17.68,-55.42 z"
             id="path21"
             inkscape:connector-curvature="0"
             style="opacity:1;fill:#00abe1" />
          <path
             d="m 408.98,35.84 c 4,-0.3 8.03,-0.26 12.04,-0.04 0.17,18.79 0.28,37.62 -0.04,56.4 -3.7,1.07 -7.87,0.1 -11.74,0.47 -0.21,-18.93 -0.52,-37.89 -0.26,-56.83 z"
             id="path23"
             inkscape:connector-curvature="0"
             style="opacity:1;fill:#00abe1" />
        </g>
      </svg>
    </li>
    <div class="secondary-buttons">Sign In</div>
    <li class="buttons">Sign Up</a>

    </div>
    <div class="main">
      <div class="area">
        <h1>Unlimited movies, TV <br>shows, and more.</h1>

        <div class="search">
          <input type="text" class="box" placeholder="Email">
          <span class="try">
            <g>
              <svg width="50" height="38" viewBox="0 0 480 480" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M461.248 194.736L333.248 66.736C308.32 41.776 267.68 41.776 242.752 66.736C230.656 78.8 224 94.896 224 111.984C224 129.072 230.656 145.168 242.752 157.232L325.504 239.984L242.752 322.736C230.656 334.832 224 350.896 224 367.984C224 385.072 230.656 401.136 242.752 413.232C254.848 425.328 270.912 431.984 288 431.984C305.088 431.984 321.152 425.328 333.248 413.232L461.248 285.232C473.344 273.168 480 257.072 480 239.984C480 222.896 473.344 206.8 461.248 194.736ZM438.624 262.608L310.624 390.608C298.496 402.704 277.504 402.704 265.376 390.608C252.896 378.128 252.896 357.84 265.376 345.36L370.752 239.984L265.376 134.608C259.328 128.56 256 120.528 256 111.984C256 103.44 259.328 95.408 265.376 89.36C271.616 83.12 279.808 79.984 288 79.984C296.192 79.984 304.384 83.12 310.624 89.328L438.624 217.328C444.672 223.408 448 231.44 448 239.984C448 248.528 444.672 256.56 438.624 262.608Z" fill="white"/>
                <path d="M237.248 194.736L109.248 66.736C84.32 41.776 43.68 41.776 18.752 66.736C6.656 78.8 0 94.896 0 111.984C0 129.072 6.656 145.168 18.752 157.232L101.504 239.984L18.752 322.736C6.656 334.832 0 350.896 0 367.984C0 385.072 6.656 401.136 18.752 413.232C30.848 425.328 46.912 431.984 64 431.984C81.088 431.984 97.152 425.328 109.248 413.232L237.248 285.232C249.344 273.168 256 257.072 256 239.984C256 222.896 249.344 206.8 237.248 194.736ZM214.624 262.608L86.624 390.608C74.496 402.704 53.504 402.704 41.376 390.608C28.896 378.128 28.896 357.84 41.376 345.36L146.752 239.984L41.376 134.608C35.328 128.56 32 120.528 32 111.984C32 103.44 35.328 95.408 41.376 89.36C47.616 83.12 55.808 79.984 64 79.984C72.192 79.984 80.384 83.12 86.624 89.328L214.624 217.328C220.672 223.408 224 231.44 224 239.984C224 248.528 220.672 256.56 214.624 262.608Z" fill="white"/>
            </svg>
          </g>


          </span>
        </div>
        <h4>Ready to watch? Enter your email to create your account.
        </h4>
      </div>

    </div>
    
  </body>
  </html>
