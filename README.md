<!DOCTYPE html>
<html>
<head>
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <link rel="apple-touch-icon" sizes="152x152" href="apple-touch-icon-152x152.png">
   <title>かいさんボタン</title>
   <meta name="apple-mobile-web-app-capable" content="yes" />
   <meta name="apple-mobile-web-app-status-bar-style" content="default">
   <style>
       html, body {
           margin: 0;
           padding: 0;
           overflow: hidden;
       }

       img {
           position: fixed;
           top: 0;
           left: 0;
           width: 100%;
           height: 100%;
           object-fit: fill;
           z-index: 9999;
       }
   </style>
   <script>
       function playSoundAndChangeImage() {
           var audio = new Audio('sound.mp3');
           audio.play();

           var image = document.getElementById('myImage');
           var originalSrc = image.src;

           image.src = 'newImage.png';

           setTimeout(function() {
               image.src = originalSrc;
           }, 3000);
       }
   </script>
</head>
<body>
   <img id="myImage" src="oldImage.png" alt="ボタン画像" onclick="playSoundAndChangeImage()">
</body>
</html>
