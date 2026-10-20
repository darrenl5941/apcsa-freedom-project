# Tool Learning Log

## Tool: **ml5.js** and **Firebase**

## Project: **Turn working out (calisthenics) into a videogame**

---

### 10/19/2026:
* https://docs.ml5js.org/#/
    * **CDN Script Tag** : `https://unpkg.com/ml5@1/dist/ml5.min.js`
        * `https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.6.0/p5.min.js` (p5.js needed for ml5.js)
        * `https://cdn.jsdelivr.net/npm/p5.sound@0.4.1/dist/p5.sound.min.js` (p5.sound)
    * `let video;`: for the camera / webcam
        * Full setup:
        ```js
        let video; // for the camera / webcam
        video = createCapture(VIDEO); // to access webcam
        video.size(640, 480); // controls size shown on screen later
        video.hide(); // prevent it from being put on screen too early
        ```




<!-- ### X/X/XX:
* Text -->


<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
