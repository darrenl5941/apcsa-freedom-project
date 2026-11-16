# Entry 1
##### 11/9/2026

### Introduction

For my Freedom Project this year I am using `ml5.js`, a javascript motion tracking library. The reason I chose `ml5.js` is because I want to use motion tracking to turn working out into a videogame as a way to convince more people to work out and benefit their health. 

### Researching and Practicing ml5.js

When researching for tools for my project I came across two motion tracking libraries, [Google Media Pipe](https://developers.google.com/edge/mediapipe/solutions/vision/pose_landmarker) and [ml5.js](https://ml5js.org/). I ended up deciding to use _ml5.js_ as it was a lot more easily accesable and many of it's motion tracking was actually the exact same as _Google Media Pipe_'s.

To start practicing using _ml5.js_ I first had to put their **CDN Key** (`https://unpkg.com/ml5@1/dist/ml5.min.js`) allong with the one for  _p5.js_ (`https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.6.0/p5.min.js`) as _ml5.js_ is based off of _p5.js_.

Once I set up the CDN Key's I had to set up the camera and the screen to display it:

```js
console.log("ml5 version:", ml5.version);
video = createCapture(VIDEO); // to access webcam
video.size(640, 480); // controls size shown on screen later
video.hide(); // prevent it from being put on screen too early

//...

createCanvas(1200, 800); // width, height
```

Before practicing with the full body motion tracking which is more complicated I decided to [tinker](https://github.com/darrenl5941/apcsa-freedom-project/blob/main/tool/ml5js-practice.html) with their **hand motioin tracking** (`handPose()`).

After following the [tutorial](https://docs.ml5js.org/#/) for all of the things above, I decided to put [dots on all of the points it was tracking](https://darrenl5941.github.io/apcsa-freedom-project/tool/ml5js-practice.html):

```js
if(hands.length > 0) {
    let hand = hands[0]; // get array of the first hand
    fill(255, 0, 0);
    noStroke();

    for (let i = 0; i < hand.keypoints.length; i++) {
        let point = hand.keypoints[i];
        circle(point.x, point.y, 10);
    }
}
```

### Engineering Design Process

I have currently completed the **1st** part of the Engineering Design Process, defining what I am trying to do (use motion tracking with working out), and am currently working on the **2nd** part of the Engineering Design Process, researching how to use my tool to do this.

### Skills

One of the skills that I have learned over the course of this blog is **debugging**. While learning my tool I have had to debug and solve issues many times, like my `ml5.js` CDN key not working because I didn't include  the `p5.js` CDN key, the camera not formatting properly because of incorrect sizing, and the program not working on some devices. Debugging is an extremely important skill as not everything will work on your first attept, and you need to be able to figure out what is causing the issue and how to solve it.

Another skill that I have learned is **how to learn**. Learning how `ml5.js` is something that I have had to research and learn on my own, leading to me having to experiment with code instead of following set instructions.



<!-- Text -->

[Next](entry02.md)

[Home](../README.md)