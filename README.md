# 60 FPS (in) Cookie Clicker
## This script sets the game's internal FPS value to 60, making it 60 FPS with the side effect of making it sped-up
You can use it in a userscript extension like Greasemonkey or Tampermonkey with the following userscript:
```
// ==UserScript==
// @name         60 FPS
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  Sets the game's internal FPS to 60
// @author       TheEeveeLovers
// @match        https://orteil.dashnet.org/cookieclicker/
// @icon         https://www.google.com/s2/favicons?sz=64&domain=dashnet.org
// @run-at       document-idle
// @grant unsafeWindow
// ==/UserScript==
(function() {
    var checkReady = setInterval(function() {
        if (typeof Game.ready !== 'undefined' && Game.ready) {
            Game.LoadMod('https://theeeveelovers.github.io/60-fps-CC/60FPS.js');
            clearInterval(checkReady);
        }
    }, 1000);
})();
```
<br></br>

## Comparison videos (GitHub Pages only)

### Normal Speed

<video width="320" height="240" autoplay loop>
  <source src="https://i.imgur.com/nXszGhA.mp4" type="video/mp4">
  <h3>Your browser does not support the video tag.</h3>
</video>

### x2 Speed

<video width="320" height="240" autoplay loop>
  <source src="https://i.imgur.com/xYGwwt6.mp4" type="video/mp4">
  <h3>Your browser does not support the video tag.</h3>
</video>

<br></br>

## Planned changes
- Change name to 'Sped Up Cookie Clicker'
- Ability to customize overriden FPS value
- Better GitHub Pages page
- Seperate (adjective) FPS for different game things
