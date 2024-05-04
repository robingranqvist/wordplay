# Wordplay

Super-easy letter & word reveal animations on page load and/or scroll.

## Preview

Check out [this interface](https://shaped-by-robin.webflow.io/projects/wordplay) to try it out and fiddle with its options etc. It's kinda cool.

![Wordplay](https://github.com/robingranqvist/wordplay/blob/main/wordplay--github.jpg?raw=true)

## Usage

### Import

Import Wordplay through its CDN.

```javascript
<script src="https://cdn.jsdelivr.net/gh/robingranqvist/wordplay@1.1.0/script.js"></script>
```

### Init

Make sure to wait for the DOM to load before initializing Wordplay.

```javascript
document.addEventListener("DOMContentLoaded", () => {
  new WordPlay({
    className: "wordplay",
    mode: "letter",
    offset: 100,
    speed: 0.5,
    delay: 0.025,
  });
});
```

### Multiple instances

Wordplay can be used for multiple different animations on the same page. Simply create a new instance for each new class you want animated.

```javascript
document.addEventListener("DOMContentLoaded", () => {
  new WordPlay({
    className: "heading",
    mode: "letter",
    offset: 100,
    speed: 0.5,
    delay: 0.025,
  });

  new WordPlay({
    className: "heading--2",
    mode: "word",
    offset: 50,
    speed: 0.25,
    delay: 0.05,
  });
});
```

### Options

#### className

This is the class name of the text element(s) you want animated.

#### mode

Wordplay has two modes - "letter" & "word".

Letter animates every single letter in a line of text while word animates each word.

#### offset (px)

The offset is used for when you want to trigger the animation when an element based on scroll. It's very similar to Webflow's native interaction offset.

#### speed

The speed of which each element (word or letter) gets revealed.

#### delay

The stagger delay between each animated word or letter.
