# Loading CSS into our React App
Can be loaded many different ways:

* Inline styles
* Separate CSS files for every single Component
* Traditional way using a Sass/CSS file and then they load it into the HTML

No problem if you just want to have `link` element and point to your CSS

## Styles for CSS and Components
Some people create CSS files for every single Component that they work on and that enables them to scope the CSS to that specific Component

### First, grab our starting assets
Images, Fonts and CSS

[github assets for this react project](https://github.com/kingluddite/starting-react-assets)

Make sure you are inside the `src` folder of your project and clone the folder without the repo name:

`$ git clone https://github.com/kingluddite/starting-react-assets.git .`

**note** When cloning, you can use `.` to say grab the repo and put all the files inside where I currently am and don't put them inside a containing folder (which is the default behavior)

### Add your style
Create `src/css/style.css` and copy and paste the following code inside that file:

```css
@font-face {
  font-family: "haymakerregular";
  src: url("./fonts/haymaker-webfont.eot");
  src: url("./fonts/haymaker-webfont.eot?#iefix") format("embedded-opentype"),
         url("./fonts/haymaker-webfont.woff") format("woff"),
         url("./fonts/haymaker-webfont.ttf") format("truetype"),
         url("./fonts/haymaker-webfont.svg#haymakerregular") format("svg");
  font-weight: normal;
  font-style: normal;
}

@font-face {
  font-family: 'blanchcaps_inline';
  src: url("./fonts/blanch_caps_inline-webfont.eot");
  src: url("./fonts/blanch_caps_inline-webfont.eot?#iefix") format('embedded-opentype'),
         url("./fonts/blanch_caps_inline-webfont.woff") format('woff'),
         url("./fonts/blanch_caps_inline-webfont.ttf") format('truetype'),
         url("./fonts/blanch_caps_inline-webfont.svg#blanchcaps_inline") format('svg');
  font-weight: normal;
  font-style: normal;
}

article, aside, details, figcaption, figure, footer, header, hgroup, nav,
section, summary {
  display: block;
}

audio, canvas, video {
  display: inline-block;
}

audio:not([controls]) {
  display: none;
  height: 0;
}

[hidden] {
  display: none;
}

html {
  font-family: sans-serif;
  -webkit-text-size-adjust: 100%;
      -ms-text-size-adjust: 100%;
}

a:focus {
  outline: thin dotted;
}

a:active, a:hover {
  outline: 0;
}

h1 {
  font-size: 2em;
}

abbr[title] {
  border-bottom: 1px dotted;
}

b, strong {
  font-weight: 700;
}

dfn {
  font-style: italic;
}

mark {
  background: #ff0;
  color: #000;
}

code, kbd, pre, samp {
  font-family: monospace, serif;
  font-size: 1em;
}

pre {
  white-space: pre-wrap;
  word-wrap: break-word;
}

q {
  quotes: 2 1C 2 1D 2 18 2 19;
}

small {
  font-size: 80%;
}

sub, sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}

sup {
  top: -0.5em;
}

sub {
  bottom: -0.25em;
}

img {
  border: 0;
}

svg:not(:root) {
  overflow: hidden;
}

fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: .35em .625em .75em;
}

button, input, select, textarea {
  font-family: inherit;
  font-size: 100%;
  margin: 0;
}

button, input {
  line-height: normal;
}

button, html input[type=button], input[type=reset], input[type=submit] {
  -webkit-appearance: button;
  cursor: pointer;
}

button[disabled], input[disabled] {
  cursor: default;
}

input[type=checkbox], input[type=radio] {
  box-sizing: border-box;
  padding: 0;
}

input[type=search] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}

input[type=search]::-webkit-search-cancel-button,
input[type=search]::-webkit-search-decoration {
  -webkit-appearance: none;
}

textarea {
  overflow: auto;
  vertical-align: top;
}

table {
  border-collapse: collapse;
  border-spacing: 0;
}

body, figure {
  margin: 0;
}

legend, button::-moz-focus-inner, input::-moz-focus-inner {
  border: 0;
  padding: 0;
}

.clearfix:after {
  visibility: hidden;
  display: block;
  font-size: 0;
  content: " ";
  clear: both;
  height: 0;
}

* {
  box-sizing: border-box;
}

html {
  font-size: 62.5%;
}

body {
  background: #d4d4d4;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-family: 'Open Sans', sans-serif;
  font-size: 2rem;
}

h1 {
  font-family: 'blanchcaps_inline', sans-serif;
  text-align: center;
  font-weight: normal;
  margin: 0;
}

h2, h3, h4, h5, h6 {
  font-weight: normal;
  font-family: 'haymakerregular', sans-serif;
}

h2 {
  text-align: center;
  margin-top: 0;
  margin-bottom: 2rem;
}

h3 {
  font-size: 3rem;
}

header.top {
  text-align: center;
}

header.top h1 {
  font-size: 14.4rem;
  line-height: .7;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  justify-content: center;
}

header.top h1 .of-the {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  font-size: 3rem;
  color: #f5a623;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  background: url("./images/anchor.svg") center no-repeat;
  background-size: cover;
  padding: 0 1rem;
}

header.top h1 .of-the .of {
  padding-right: 2rem;
  position: relative;
  right: -0.5rem;
}

header.top h3 {
  margin: 0;
  font-size: 2rem;
  color: #f5a623;
  position: relative;
  display: inline-block;
}

header.top h3 span {
  background: #fff;
  position: relative;
  z-index: 2;
  padding-left: 1rem;
  padding-right: 1rem;
}

header.top h3:before, header.top h3:after {
  display: block;
  z-index: 1;
  background: #000;
  position: absolute;
  width: 130%;
  height: 1px;
  content: '';
  top: 5px;
  margin-left: -15%;
}

header.top h3:after {
  top: auto;
  bottom: 7px;
}

.team-of-the-day {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  height: 90vh;
  max-width: 1500px;
  margin: 0 auto;
  margin-top: 5vh;
  -webkit-perspective: 1000;
          perspective: 1000;
  -webkit-transform-style: preserve-3d;
          transform-style: preserve-3d;
}

.team-of-the-day > * {
  -webkit-box-flex: 1;
  -ms-flex: 1 4 auto;
      flex: 1 4 auto;
  padding: 2rem;
  border: 1rem double #1a1a1a;
  position: relative;
  background: #fff;
  -webkit-transition: all .3s;
          transition: all .3s;
  box-shadow: 0 5px 5px rgba(0, 0, 0, .1);
  overflow: scroll;
}

.team-of-the-day > *:first-child {
  -ms-flex-negative: 1;
  flex-shrink: 1;
  -ms-flex-preferred-size: 50%;
  flex-basis: 50%;
  -webkit-transform: translateX(50%) rotateY(6deg) translateX(-50%);
          transform: translateX(50%) rotateY(6deg) translateX(-50%);
}

.team-of-the-day > *:nth-child(2) {
  -webkit-transform: translateX(-50%) rotateY(-14deg) translateX(50%);
          transform: translateX(-50%) rotateY(-14deg) translateX(50%);
  border-left: 0;
  border-right: 0;
  min-width: 300px;
}

.team-of-the-day > *:last-child {
  -ms-flex-negative: 1;
  flex-shrink: 1;
  -ms-flex-preferred-size: 50%;
  flex-basis: 50%;
  -webkit-transform: translateX(-50%) rotateY(10deg) translateX(50%) scale(1.08) translateX(24px);
          transform: translateX(-50%) rotateY(10deg) translateX(50%) scale(1.08) translateX(24px);
}

input#fold:not(:checked) ~ #main .team-of-the-day > * {
  -webkit-transform: none;
          transform: none;
}

label[for="fold"] {
  position: absolute;
  top: 1rem;
  left: 1rem;
  text-transform: uppercase;
  font-size: 1.3rem;
  background: #000;
  color: #fff;
  border: 2px solid #000;
  cursor: pointer;
  padding: .5rem 1rem;
}

input#fold {
  display: none;
}

input#fold:checked + label {
  background: #fff;
  color: #000;
}

ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

ul.lineup li {
  border-bottom: 1px solid #000;
  padding: 2rem 0;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  font-size: 1.4rem;
  -webkit-box-pack: justify;
  -ms-flex-pack: justify;
  justify-content: space-between;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
}

ul.lineup li:hover button {
  display: inline;
}

ul.lineup li button {
  border: 0;
  display: none;
  line-height: 1;
  padding: 0;
}

ul.lineup li.total {
  font-weight: 600;
  border-bottom: 3px solid #000;
  border-top: 3px double #000;
}

ul.lineup li.unavailable {
  text-decoration: line-through;
  background: #f8d0d2;
}

ul.lineup li .price {
  font-size: 1.2rem;
}

ul.lineup li span.count {
  position: relative;
  overflow: hidden;
  float: left;
}

ul.lineup li span.count span {
  display: inline-block;
}

.order-title {
  text-align: center;
}

.player-edit {
  margin-bottom: 20px;
  border: 2px solid #000;
  overflow: hidden;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -ms-flex-wrap: wrap;
      flex-wrap: wrap;
}

.player-edit input, .player-edit textarea, .player-edit select {
  width: 33.33%;
  padding: 10px;
  line-height: 1;
  font-size: 1.2rem;
  border: 0;
  border-bottom: 1px solid #000;
  border-right: 1px solid #000;
  -webkit-appearance: none;
     -moz-appearance: none;
          appearance: none;
  border-radius: 0;
  background: #fff;
}

.player-edit input:focus, .player-edit textarea:focus, .player-edit select:focus {
  outline: 0;
  background: #fef2de;
}

.player-edit textarea {
  width: 100%;
}

.player-edit input:last-of-type {
  width: 100%;
}

.player-edit button {
  width: 100%;
  border: 0;
}

.list-of-fish {
  border-top: 2px solid #000;
  border-bottom: 1px solid #000;
  padding-top: 5px;
  margin-top: 2rem;
  -webkit-transform: translateZ(0);
          transform: translateZ(0);
}

.menu-player {
  border-bottom: 2px solid #000;
  border-top: 1px solid #000;
  padding-bottom: 2rem;
  padding-top: 2rem;
  margin-bottom: 5px;
  clear: both;
  overflow: hidden;
}

.menu-player p {
  margin: 0;
  font-size: 1.8rem;
}

.menu-player .player-name {
  margin: 0;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: justify;
  -ms-flex-pack: justify;
  justify-content: space-between;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
}

.menu-player .price {
  font-size: 1.4rem;
  -webkit-box-pack: end;
  -ms-flex-pack: end;
  justify-content: flex-end;
}

.menu-player img {
  float: left;
  width: 150px;
  margin-right: 1rem;
}

button, input[type=submit] {
  text-transform: uppercase;
  background: none;
  border: 1px solid #000;
  font-weight: 600;
  font-size: 1.5rem;
  font-family: 'Open Sans';
  -webkit-transition: all .2s;
          transition: all .2s;
  position: relative;
  z-index: 2;
}

button[disabled], input[type=submit][disabled] {
  color: #d12028;
  background: #fff;
  border-color: #d12028;
  -webkit-transform: rotate(-10deg) scale(2) translateX(50%) translateY(-50%);
          transform: rotate(-10deg) scale(2) translateX(50%) translateY(-50%);
}

button[disabled]:hover, input[type=submit][disabled]:hover {
  color: #d12028;
  cursor: not-allowed;
}

button[disabled]:after, input[type=submit][disabled]:after {
  display: none;
}

button:after, input[type=submit]:after {
  content: '';
  z-index: -1;
  display: block;
  background: #000;
  position: absolute;
  width: 100%;
  height: 0%;
  left: 0;
  top: 0;
  -webkit-transition: all .2s;
          transition: all .2s;
}

button:hover, input[type=submit]:hover, button:focus, input[type=submit]:focus {
  color: #fff;
  outline: 0;
}

button:hover:after, input[type=submit]:hover:after, button:focus:after,
input[type=submit]:focus:after {
  height: 100%;
}

button.warning:after, input[type=submit].warning:after {
  background: #d12028;
}

button.success:after, input[type=submit].success:after {
  background: #2dc22d;
}

button.github, input[type=submit].github, button.facebook,
input[type=submit].facebook, button.twitter, input[type=submit].twitter {
  border: 0;
  display: block;
  margin-bottom: 2rem;
  width: 100%;
  color: #fff;
  padding: 2rem;
}

button.github, input[type=submit].github {
  background: #82d465;
}

button.github:after, input[type=submit].github:after {
  background: #5cc437;
}

button.facebook, input[type=submit].facebook {
  background: #3864a3;
}

button.facebook:after, input[type=submit].facebook:after {
  background: #2d5082;
}

button.twitter, input[type=submit].twitter {
  background: #5ea9dd;
}

button.twitter:after, input[type=submit].twitter:after {
  background: #2c8dd0;
}

.team-selector {
  background: #fff;
  max-width: 500px;
  margin: 50px auto;
  padding: 2rem;
  border: 2px solid #000;
}

.team-selector input, .team-selector button {
  width: 100%;
}

.team-selector input[type="text"], .team-selector button[type="text"] {
  text-align: center;
  font-size: 3rem;
}
```

## Load CSS using Webpack
Don't add `link` tag to `index.html` manually. Import the css into the `index.js` file like this:

`index.js`

```
import React from 'react';
import { render } from 'react-dom';
import './css/style.css'; // Add this line
```

**note** We don't say the name of the package we are loading for `style.css` because there is no package. We are just loading the file

**important** Remove in `index.html` the `<link href="css/style.css >` and add the import line above to let webpack import all the css. You won't see a css file but if you search the `bundle.min.js` you will see the css is inside that JavaScript file!