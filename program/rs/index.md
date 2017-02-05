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
  var reds = [255, 0, 0]
  var greens = [0, 255, 0]
  var blues = [0, 0, 255]
  var yellows = [255, 255, 0]
  var colors = [ reds, greens, blues, yellows]

  var offset = 185;
  var offset1 = 190;

  function r(offset, colors) {
    var r = parseInt(random(4));
    fill(colors[r])
    rect(125 + offset, 200, 50, 50);
    rect(125 + offset, 250, 50, 50);
    rect(75 + offset, 200, 50, 50);
    rect(25 + offset, 250, 50, 50);
    rect(25 + offset, 300, 50, 50);
    rect(25 + offset, 350, 50, 50);
    rect(25 + offset, 400, 50, 50);
  }

  function s(offset, colors) {
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
  }

  function setup()
  {
    if(windowWidth < 1050) {
      var canvas = createCanvas(windowWidth - windowWidth / 5, 600);
    } else {
      var canvas = createCanvas(800, 500);
    }
    canvas.parent('sketch-holder');
    background(255, 255, 255)
    blendMode(DIFFERENCE); //http://p5js.org/reference/#/p5/blendMode
    frameRate(0.7);
    r(offset, colors);
    s(offset, colors);
    r(offset1, colors);
    s(offset1, colors);    
  }

  function draw() {
    r(offset, colors);
    s(offset, colors);
    r(offset1, colors);
    s(offset1, colors);
  }
</script>
