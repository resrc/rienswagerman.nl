<style>
  html, body {
   background-color: rgb(255, 255, 255);
}
.sketches canvas {
  margin-left: -40px;
}

</style>

<script src="//cdnjs.cloudflare.com/ajax/libs/p5.js/0.5.6/p5.js"></script>
<div id="sketch-holder" class="sketches">
    <!-- Our sketch will go here! -->
</div>
<script>
  function setup()
  {
    if(windowWidth < 1050) {
      var canvas = createCanvas(windowWidth - windowWidth / 5, 600);
    } else {
      var canvas = createCanvas(800, 500);
    }
    canvas.parent('sketch-holder');
    background(255, 255, 255)
    //noLoop();
    blendMode(DIFFERENCE); //http://p5js.org/reference/#/p5/blendMode
    frameRate(0.7);
  }

  var reds = [255, 0, 0]
  var greens = [0, 255, 0]
  var blues = [0, 0, 255]
  var yellows = [255, 255, 0]
  var colors = [ reds, greens, blues, yellows]

  var offset = 185;
  var offset1 = 190;

  function draw() {
    //console.log(parseInt(mouseX/100))
    var r = parseInt(random(4));
    fill(colors[r])
    rect(125 + offset, 200, 50, 50);
    rect(125 + offset, 250, 50, 50);
    rect(75 + offset, 200, 50, 50);
    rect(25 + offset, 250, 50, 50);
    rect(25 + offset, 300, 50, 50);
    rect(25 + offset, 350, 50, 50);
    rect(25 + offset, 400, 50, 50);
    var r = parseInt(random(4));
    fill(colors[r])
    rect(325 + offset, 200, 50, 50);    
    rect(275 + offset, 200, 50, 50);    
    rect(225 + offset, 250, 50, 50);    
    rect(225 + offset, 300, 50, 50);    
    rect(275 + offset, 300, 50, 50);    
    rect(325 + offset, 350, 50, 50);    
    rect(325 + offset, 400, 50, 50);    
    rect(275 + offset, 400, 50, 50);    
    rect(225 + offset, 400, 50, 50);  


    var r = parseInt(random(4));
    fill(colors[r])
    rect(125 + offset1, 200, 50, 50);
    rect(125 + offset1, 250, 50, 50);
    rect(75 + offset1, 200, 50, 50);
    rect(25 + offset1, 250, 50, 50);
    rect(25 + offset1, 300, 50, 50);
    rect(25 + offset1, 350, 50, 50);
    rect(25 + offset1, 400, 50, 50);
    var r = parseInt(random(4));
    fill(colors[r])
    rect(325 + offset1, 200, 50, 50);    
    rect(275 + offset1, 200, 50, 50);    
    rect(225 + offset1, 250, 50, 50);    
    rect(225 + offset1, 300, 50, 50);    
    rect(275 + offset1, 300, 50, 50);    
    rect(325 + offset1, 350, 50, 50);    
    rect(325 + offset1, 400, 50, 50);    
    rect(275 + offset1, 400, 50, 50);    
    rect(225 + offset1, 400, 50, 50);      
  }
</script>

<!--<small style="text-align: center; width: 100%; display: inline-block;">rs - modeled in p5.js.</small>-->

