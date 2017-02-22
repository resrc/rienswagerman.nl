---
title: Colour Sounds - Karl Gerstner
description: Digital program of the Colour Sounds from Karl Gerstner.
og_image: http://www.rienswagerman.nl/program/rs/assets/rs.png
content_type: sketch
---

<style>
  html, body {
   background-color: rgb(100, 134, 233);
  }
</style>

<script src="//cdnjs.cloudflare.com/ajax/libs/p5.js/0.5.6/p5.js"></script>

<div id="sketch-holder" class="sketches">
      <!-- sketch will go here! -->
</div>

<script>
  function setup()
  {

    var canvas = createCanvas(800, 800);
    canvas.parent('sketch-holder');
    background(100, 134, 233)
    noLoop();
    //blendMode(SOFT_LIGHT); //http://p5js.org/reference/#/p5/blendMode
    var w = width * 0.9;
    var h = height * 0.9;
    translate((width/2) - (w/2), (height/2) - (h/2));
    drawBottomItems(w, h, 5);
    drawTopItems(w, h, 4);
  }

  function drawTopItems(w, h, level) {
      var offset = - 4 * level;
      var size = 660 - 16;
      var size_rect_bottom = 230;
      var compensate_prev_levels = 4 * 4
      var offset_bottom_gap =  80 * level;
      var bottom_gap = 50 + offset_bottom_gap;

      stroke(0);
      strokeWeight(0);

      beginShape();
        fill(255 - 5 * level, 130 - 5 * level, 20 - 5 * level);

        vertex(size_rect_bottom + compensate_prev_levels + offset, size - offset);
        vertex(size_rect_bottom*2 - compensate_prev_levels - offset, size - offset);
        vertex(size_rect_bottom*2 - compensate_prev_levels - offset, size - size_rect_bottom - bottom_gap);
        vertex(size_rect_bottom + compensate_prev_levels + offset, size - size_rect_bottom - bottom_gap);
      endShape();

      level = level - 1;
      if(level > 0) {
        console.log("level", level)
        drawTopItems(w, h, level)
      }
  }


  function drawBottomItems(w, h, level) {
    var offset = - 4 * level;
    var offset_bottom_gap = 400 - 80 * level;
    var bottom_gap = 50 + offset_bottom_gap;
    var size = 660;
    var size_rect_bottom = 230;

    stroke(0);
    strokeWeight(0);

    beginShape();
      fill(160 - 10 * level, 134, 233)
      
      vertex(60 + offset, 60 + offset); 
      vertex(60 + offset, size-bottom_gap); 
      vertex(size_rect_bottom + offset, size-bottom_gap);
      //rect down 
      vertex(size_rect_bottom + offset, size - offset);
      vertex(size_rect_bottom*2 - offset, size - offset);
      vertex(size_rect_bottom*2 - offset, size-bottom_gap);
      //
      vertex(size - offset, size-bottom_gap);
      //top right
      vertex(size - offset, 60 + offset);
    endShape();

    level = level - 1;
    if(level > 0) {
      console.log("level", level)
      drawBottomItems(w, h, level)
    }
  }
</script>


<small style="text-align: center; width: 100%; display: inline-block;">Colour Sounds - Karl Gerstner.</small>
