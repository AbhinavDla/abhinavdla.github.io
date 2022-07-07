<!DOCTYPE html>
<!-- This is based on DillingerLee's great template here:
https://github.com/Team-Code/KA_Offline -->
<html> 
 <head>
    <title>Processing.JS inside Webpages: Template</title> 

</head>
 <body>
    <p align="center"> 
	<!--This draws the Canvas on the webpage -->
      <canvas id="mycanvas" width="170000000" height="1700"> </canvas>
    </p>
 </body>
 
 <!-- Run all the JavaScript stuff -->
 <!-- Include the processing.js library -->
 <!-- See https://khanacademy.zendesk.com/hc/en-us/articles/202260404-What-parts-of-ProcessingJS-does-Khan-Academy-support- for differences -->
 <script src="https://cdn.jsdelivr.net/processing.js/1.4.8/processing.min.js"></script> 
 
 <script>
    var sketchProc = function(processingInstance) {
     with (processingInstance) {
        mouseDragged = function() {
        fill(255, 0, 0);
        ellipse(mouseX, mouseY, 1, 1);
        
        };
    }};

    // Get the canvas that Processing-js will use
    var canvas = document.getElementById("mycanvas"); 
    // Pass the function sketchProc (defined in myCode.js) to Processing's constructor.
    var processingInstance = new Processing(canvas, sketchProc); 
 </script>

</html>
