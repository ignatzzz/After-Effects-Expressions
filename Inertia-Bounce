// Inertial Bounce - Created by Animoplex: www.animoplex.com
// Original Version: http://www.graymachine.com/top-5-effects-expressions/
// Modified expression for a smoother bounce effect and easier editing. Use this on any property with two keyframes to get a nice bounce effect that is based on velocity of the value change. Perfect for a scale from 0 to 100 or a speedy rotation that needs some extra life. Adjust amp, freq and decay values to tweak the effect. Amp is intensity, freq is bounces per second, and decay is the speed of decay, slow to fast.
// Full Tutorial: https://www.youtube.com/watch?v=653lxeVIyoo

amp = 5.0; freq = 2.0; decay = 4.0;

n = 0;
if (numKeys > 0) {
  n = nearestKey(time).index;
  if (key(n).time > time) { n--; }
}
if (n == 0) {
  t = 0;
} else {
  t = time - key(n).time;
}
if (n > 0 && t < 1) {
  v = velocityAtTime(key(n).time - thisComp.frameDuration/10);
  value + v*(amp/100)*Math.sin(freq*t*2*Math.PI)/Math.exp(decay*t);
} else {
  value;
}
