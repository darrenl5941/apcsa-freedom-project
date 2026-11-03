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
### 11/02/2026
* https://docs.ml5js.org/#/
    * `async` (tag): makes a function asynchronous
        * `await` (tag): wait for thing to fully load before running
    * `handPose.detectStart(video, gotHands);` (example): `.detectstart` works on the variable once the input runs and puts it through the function
        * First parameter is the input, usually the video/camera
        * Second parameter is the function that the input runs through
    * `hands` (array): includes 21 different points in the hand
        * [0] wrist
        * Thumb: `[1] thumb_cmc` `[2] thumb_mcp` `[3] thumb_ip` `[4] thumb_tip`
        * Index Finger: `[5] index_finger_mcp` `[6] index_finger_pip` `[7] index_finger_dip` `[8] index_finger_tip`
        * Middle Finger: `[9] middle_finger_mcp` `[10] middle_finger_pip` `[11] middle_finger_dip` `[12] middle_finger_tip`
        * Ring Finger: `[13] ring_finger_mcp` `[14] ring_finger_pip` `[15] ring_finger_dip` `[16] ring_finger_tip`
        * Pinky: `[17] pinky_mcp` `[18] pinky_pip` `[19] pinky_dip` `[20] pinky_tip`
    * `image`: creates an image on screen (usually used to show the camera)
    * `createCanvas` (p5.js): use to control the size of the screen displayed (without htis default is `(100, 100)` which does not fit properly)
    * Getting position of something on screen (in this example the `index_finger_tip` on a `hand`):
    ```js
    // Check if there is at least one hand detected
    if (hands.length > 0) {
    
    // Get the index finger tip and thumb of the first hand (index: 0 in the array)
    let fingerX = hands[0].index_finger_tip.x;
    let fingerY = hands[0].index_finger_tip.y;
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
