# code-demo-css3-animation

# HTML Files
1. **start.html:** basic html code for header and navbar, instructions in the comments throughout the document.
2. **finished.html:** animated header and navbar. this is what it should be like after completing the code demo.

# CSS Files
1. **css/startstyles.css:** basic css for header and navbar style, animation code needed from 'copystyles.css'
2. **css/copystyles.css:** animation code snippets that will add animation, copy/paste into 'startstyles.css'.
3. **css/styles.css:** style sheet for finished.html to see what the animations should look like at the end.
4. **css/animate.css:** allows use of the Animate.css Library found at <http://daneden.me/animate>.

# copystyles.css
CSS code snippets that can be copy/paste into **startstyles.css**.

(4) Timing for header animation 
```css
header {
  -webkit-animation-duration: 0.5s; /* Header animation will take 0.5s to complete. */
          animation-duration: 0.5s;
  -webkit-animation-delay: 0.5s; /* Header animation will begin 0.5s after the page loads */
          animation-delay: 0.5s;
}
```
(5a) Navbar animation and timing
```css
.navbar ul{
  -webkit-animation: navstretch ease-out 1s; /* navbar animation linked to animation @keyframes named navstretch (below) */
  animation: navstretch ease-out 1s; 
  -webkit-animation-delay: 1.3s; /* Delay start of animation until header animation is complete */
  animation-delay: 1.3s; 
  -webkit-animation-iteration-count: 1; /* navstretch animation plays through 1 time */
  animation-iteration-count: 1; 
  -webkit-animation-fill-mode: forwards; /* Keeps animation from resetting to how it was at the start */
  animation-fill-mode: forwards; 
}
```
(5b) Navbar animation @keyframes
```css
@keyframes navstretch {
  0% {
    opacity: 0;
    visibility: hidden;
    transform: scaleX(0);
  }
  2% {
    opacity: 1;
    visibility: visible;
    transform: scaleX(0);
  }
  100% {
    opacity: 1;
    visibility: visible;
    transform: scaleX(1);
  }
}
@-webkit-keyframes navstretch {
  0% {
    opacity: 0;
    visibility: hidden;
    -webkit-transform: scaleX(0);
  }
  2% {
    opacity: 1;
    visibility: visible;
    -webkit-transform: scaleX(0);
  }
  100% {
    opacity: 1;
    visibility: visible;
    -webkit-transform: scaleX(1);
  }
}
```


