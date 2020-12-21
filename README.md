<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />

<title>Wine Analysis</title>

<script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>



<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
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
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.7.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.7.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.7.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff2?v=4.7.0') format('woff2'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.7.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.7.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.7.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.fa-pull-left {
  float: left;
}
.fa-pull-right {
  float: right;
}
.fa.fa-pull-left {
  margin-right: .3em;
}
.fa.fa-pull-right {
  margin-left: .3em;
}
/* Deprecated as of 4.4.0 */
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
.fa-pulse {
  -webkit-animation: fa-spin 1s infinite steps(8);
  animation: fa-spin 1s infinite steps(8);
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=1)";
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2)";
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=3)";
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1)";
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1)";
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook-f:before,
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-feed:before,
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before,
.fa-gratipay:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper-pp:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-resistance:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-y-combinator-square:before,
.fa-yc-square:before,
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
.fa-buysellads:before {
  content: "\f20d";
}
.fa-connectdevelop:before {
  content: "\f20e";
}
.fa-dashcube:before {
  content: "\f210";
}
.fa-forumbee:before {
  content: "\f211";
}
.fa-leanpub:before {
  content: "\f212";
}
.fa-sellsy:before {
  content: "\f213";
}
.fa-shirtsinbulk:before {
  content: "\f214";
}
.fa-simplybuilt:before {
  content: "\f215";
}
.fa-skyatlas:before {
  content: "\f216";
}
.fa-cart-plus:before {
  content: "\f217";
}
.fa-cart-arrow-down:before {
  content: "\f218";
}
.fa-diamond:before {
  content: "\f219";
}
.fa-ship:before {
  content: "\f21a";
}
.fa-user-secret:before {
  content: "\f21b";
}
.fa-motorcycle:before {
  content: "\f21c";
}
.fa-street-view:before {
  content: "\f21d";
}
.fa-heartbeat:before {
  content: "\f21e";
}
.fa-venus:before {
  content: "\f221";
}
.fa-mars:before {
  content: "\f222";
}
.fa-mercury:before {
  content: "\f223";
}
.fa-intersex:before,
.fa-transgender:before {
  content: "\f224";
}
.fa-transgender-alt:before {
  content: "\f225";
}
.fa-venus-double:before {
  content: "\f226";
}
.fa-mars-double:before {
  content: "\f227";
}
.fa-venus-mars:before {
  content: "\f228";
}
.fa-mars-stroke:before {
  content: "\f229";
}
.fa-mars-stroke-v:before {
  content: "\f22a";
}
.fa-mars-stroke-h:before {
  content: "\f22b";
}
.fa-neuter:before {
  content: "\f22c";
}
.fa-genderless:before {
  content: "\f22d";
}
.fa-facebook-official:before {
  content: "\f230";
}
.fa-pinterest-p:before {
  content: "\f231";
}
.fa-whatsapp:before {
  content: "\f232";
}
.fa-server:before {
  content: "\f233";
}
.fa-user-plus:before {
  content: "\f234";
}
.fa-user-times:before {
  content: "\f235";
}
.fa-hotel:before,
.fa-bed:before {
  content: "\f236";
}
.fa-viacoin:before {
  content: "\f237";
}
.fa-train:before {
  content: "\f238";
}
.fa-subway:before {
  content: "\f239";
}
.fa-medium:before {
  content: "\f23a";
}
.fa-yc:before,
.fa-y-combinator:before {
  content: "\f23b";
}
.fa-optin-monster:before {
  content: "\f23c";
}
.fa-opencart:before {
  content: "\f23d";
}
.fa-expeditedssl:before {
  content: "\f23e";
}
.fa-battery-4:before,
.fa-battery:before,
.fa-battery-full:before {
  content: "\f240";
}
.fa-battery-3:before,
.fa-battery-three-quarters:before {
  content: "\f241";
}
.fa-battery-2:before,
.fa-battery-half:before {
  content: "\f242";
}
.fa-battery-1:before,
.fa-battery-quarter:before {
  content: "\f243";
}
.fa-battery-0:before,
.fa-battery-empty:before {
  content: "\f244";
}
.fa-mouse-pointer:before {
  content: "\f245";
}
.fa-i-cursor:before {
  content: "\f246";
}
.fa-object-group:before {
  content: "\f247";
}
.fa-object-ungroup:before {
  content: "\f248";
}
.fa-sticky-note:before {
  content: "\f249";
}
.fa-sticky-note-o:before {
  content: "\f24a";
}
.fa-cc-jcb:before {
  content: "\f24b";
}
.fa-cc-diners-club:before {
  content: "\f24c";
}
.fa-clone:before {
  content: "\f24d";
}
.fa-balance-scale:before {
  content: "\f24e";
}
.fa-hourglass-o:before {
  content: "\f250";
}
.fa-hourglass-1:before,
.fa-hourglass-start:before {
  content: "\f251";
}
.fa-hourglass-2:before,
.fa-hourglass-half:before {
  content: "\f252";
}
.fa-hourglass-3:before,
.fa-hourglass-end:before {
  content: "\f253";
}
.fa-hourglass:before {
  content: "\f254";
}
.fa-hand-grab-o:before,
.fa-hand-rock-o:before {
  content: "\f255";
}
.fa-hand-stop-o:before,
.fa-hand-paper-o:before {
  content: "\f256";
}
.fa-hand-scissors-o:before {
  content: "\f257";
}
.fa-hand-lizard-o:before {
  content: "\f258";
}
.fa-hand-spock-o:before {
  content: "\f259";
}
.fa-hand-pointer-o:before {
  content: "\f25a";
}
.fa-hand-peace-o:before {
  content: "\f25b";
}
.fa-trademark:before {
  content: "\f25c";
}
.fa-registered:before {
  content: "\f25d";
}
.fa-creative-commons:before {
  content: "\f25e";
}
.fa-gg:before {
  content: "\f260";
}
.fa-gg-circle:before {
  content: "\f261";
}
.fa-tripadvisor:before {
  content: "\f262";
}
.fa-odnoklassniki:before {
  content: "\f263";
}
.fa-odnoklassniki-square:before {
  content: "\f264";
}
.fa-get-pocket:before {
  content: "\f265";
}
.fa-wikipedia-w:before {
  content: "\f266";
}
.fa-safari:before {
  content: "\f267";
}
.fa-chrome:before {
  content: "\f268";
}
.fa-firefox:before {
  content: "\f269";
}
.fa-opera:before {
  content: "\f26a";
}
.fa-internet-explorer:before {
  content: "\f26b";
}
.fa-tv:before,
.fa-television:before {
  content: "\f26c";
}
.fa-contao:before {
  content: "\f26d";
}
.fa-500px:before {
  content: "\f26e";
}
.fa-amazon:before {
  content: "\f270";
}
.fa-calendar-plus-o:before {
  content: "\f271";
}
.fa-calendar-minus-o:before {
  content: "\f272";
}
.fa-calendar-times-o:before {
  content: "\f273";
}
.fa-calendar-check-o:before {
  content: "\f274";
}
.fa-industry:before {
  content: "\f275";
}
.fa-map-pin:before {
  content: "\f276";
}
.fa-map-signs:before {
  content: "\f277";
}
.fa-map-o:before {
  content: "\f278";
}
.fa-map:before {
  content: "\f279";
}
.fa-commenting:before {
  content: "\f27a";
}
.fa-commenting-o:before {
  content: "\f27b";
}
.fa-houzz:before {
  content: "\f27c";
}
.fa-vimeo:before {
  content: "\f27d";
}
.fa-black-tie:before {
  content: "\f27e";
}
.fa-fonticons:before {
  content: "\f280";
}
.fa-reddit-alien:before {
  content: "\f281";
}
.fa-edge:before {
  content: "\f282";
}
.fa-credit-card-alt:before {
  content: "\f283";
}
.fa-codiepie:before {
  content: "\f284";
}
.fa-modx:before {
  content: "\f285";
}
.fa-fort-awesome:before {
  content: "\f286";
}
.fa-usb:before {
  content: "\f287";
}
.fa-product-hunt:before {
  content: "\f288";
}
.fa-mixcloud:before {
  content: "\f289";
}
.fa-scribd:before {
  content: "\f28a";
}
.fa-pause-circle:before {
  content: "\f28b";
}
.fa-pause-circle-o:before {
  content: "\f28c";
}
.fa-stop-circle:before {
  content: "\f28d";
}
.fa-stop-circle-o:before {
  content: "\f28e";
}
.fa-shopping-bag:before {
  content: "\f290";
}
.fa-shopping-basket:before {
  content: "\f291";
}
.fa-hashtag:before {
  content: "\f292";
}
.fa-bluetooth:before {
  content: "\f293";
}
.fa-bluetooth-b:before {
  content: "\f294";
}
.fa-percent:before {
  content: "\f295";
}
.fa-gitlab:before {
  content: "\f296";
}
.fa-wpbeginner:before {
  content: "\f297";
}
.fa-wpforms:before {
  content: "\f298";
}
.fa-envira:before {
  content: "\f299";
}
.fa-universal-access:before {
  content: "\f29a";
}
.fa-wheelchair-alt:before {
  content: "\f29b";
}
.fa-question-circle-o:before {
  content: "\f29c";
}
.fa-blind:before {
  content: "\f29d";
}
.fa-audio-description:before {
  content: "\f29e";
}
.fa-volume-control-phone:before {
  content: "\f2a0";
}
.fa-braille:before {
  content: "\f2a1";
}
.fa-assistive-listening-systems:before {
  content: "\f2a2";
}
.fa-asl-interpreting:before,
.fa-american-sign-language-interpreting:before {
  content: "\f2a3";
}
.fa-deafness:before,
.fa-hard-of-hearing:before,
.fa-deaf:before {
  content: "\f2a4";
}
.fa-glide:before {
  content: "\f2a5";
}
.fa-glide-g:before {
  content: "\f2a6";
}
.fa-signing:before,
.fa-sign-language:before {
  content: "\f2a7";
}
.fa-low-vision:before {
  content: "\f2a8";
}
.fa-viadeo:before {
  content: "\f2a9";
}
.fa-viadeo-square:before {
  content: "\f2aa";
}
.fa-snapchat:before {
  content: "\f2ab";
}
.fa-snapchat-ghost:before {
  content: "\f2ac";
}
.fa-snapchat-square:before {
  content: "\f2ad";
}
.fa-pied-piper:before {
  content: "\f2ae";
}
.fa-first-order:before {
  content: "\f2b0";
}
.fa-yoast:before {
  content: "\f2b1";
}
.fa-themeisle:before {
  content: "\f2b2";
}
.fa-google-plus-circle:before,
.fa-google-plus-official:before {
  content: "\f2b3";
}
.fa-fa:before,
.fa-font-awesome:before {
  content: "\f2b4";
}
.fa-handshake-o:before {
  content: "\f2b5";
}
.fa-envelope-open:before {
  content: "\f2b6";
}
.fa-envelope-open-o:before {
  content: "\f2b7";
}
.fa-linode:before {
  content: "\f2b8";
}
.fa-address-book:before {
  content: "\f2b9";
}
.fa-address-book-o:before {
  content: "\f2ba";
}
.fa-vcard:before,
.fa-address-card:before {
  content: "\f2bb";
}
.fa-vcard-o:before,
.fa-address-card-o:before {
  content: "\f2bc";
}
.fa-user-circle:before {
  content: "\f2bd";
}
.fa-user-circle-o:before {
  content: "\f2be";
}
.fa-user-o:before {
  content: "\f2c0";
}
.fa-id-badge:before {
  content: "\f2c1";
}
.fa-drivers-license:before,
.fa-id-card:before {
  content: "\f2c2";
}
.fa-drivers-license-o:before,
.fa-id-card-o:before {
  content: "\f2c3";
}
.fa-quora:before {
  content: "\f2c4";
}
.fa-free-code-camp:before {
  content: "\f2c5";
}
.fa-telegram:before {
  content: "\f2c6";
}
.fa-thermometer-4:before,
.fa-thermometer:before,
.fa-thermometer-full:before {
  content: "\f2c7";
}
.fa-thermometer-3:before,
.fa-thermometer-three-quarters:before {
  content: "\f2c8";
}
.fa-thermometer-2:before,
.fa-thermometer-half:before {
  content: "\f2c9";
}
.fa-thermometer-1:before,
.fa-thermometer-quarter:before {
  content: "\f2ca";
}
.fa-thermometer-0:before,
.fa-thermometer-empty:before {
  content: "\f2cb";
}
.fa-shower:before {
  content: "\f2cc";
}
.fa-bathtub:before,
.fa-s15:before,
.fa-bath:before {
  content: "\f2cd";
}
.fa-podcast:before {
  content: "\f2ce";
}
.fa-window-maximize:before {
  content: "\f2d0";
}
.fa-window-minimize:before {
  content: "\f2d1";
}
.fa-window-restore:before {
  content: "\f2d2";
}
.fa-times-rectangle:before,
.fa-window-close:before {
  content: "\f2d3";
}
.fa-times-rectangle-o:before,
.fa-window-close-o:before {
  content: "\f2d4";
}
.fa-bandcamp:before {
  content: "\f2d5";
}
.fa-grav:before {
  content: "\f2d6";
}
.fa-etsy:before {
  content: "\f2d7";
}
.fa-imdb:before {
  content: "\f2d8";
}
.fa-ravelry:before {
  content: "\f2d9";
}
.fa-eercast:before {
  content: "\f2da";
}
.fa-microchip:before {
  content: "\f2db";
}
.fa-snowflake-o:before {
  content: "\f2dc";
}
.fa-superpowers:before {
  content: "\f2dd";
}
.fa-wpexplorer:before {
  content: "\f2de";
}
.fa-meetup:before {
  content: "\f2e0";
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
div.traceback-wrapper pre.traceback {
  max-height: 600px;
  overflow: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 5px;
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
[dir="rtl"] #ipython_notebook {
  margin-right: 10px;
  margin-left: 0;
}
[dir="rtl"] #ipython_notebook.pull-left {
  float: right !important;
  float: right;
}
.flex-spacer {
  flex: 1;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#kernel_logo_widget {
  margin: 0 10px;
}
span#login_widget {
  float: right;
}
[dir="rtl"] span#login_widget {
  float: left;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
.modal-header {
  cursor: move;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
[dir="rtl"] .center-nav form.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] .center-nav .navbar-text {
  float: right;
}
[dir="rtl"] .navbar-inner {
  text-align: right;
}
[dir="rtl"] div.text-left {
  text-align: right;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
  overflow: hidden;
  cursor: pointer;
  opacity: 0;
  z-index: 2;
}
.alternate_upload .btn-xs > input.fileinput {
  margin: -1px -5px;
}
.alternate_upload .btn-upload {
  position: relative;
  height: 22px;
}
::-webkit-file-upload-button {
  cursor: pointer;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
ul#tabs {
  margin-bottom: 4px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
[dir="rtl"] ul#tabs.nav-tabs > li {
  float: right;
}
[dir="rtl"] ul#tabs.nav.nav-tabs {
  padding-right: 0;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons .pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .list_toolbar .col-sm-4,
[dir="rtl"] .list_toolbar .col-sm-8 {
  float: right;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: text-bottom;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
[dir="rtl"] .list_item > div input {
  margin-right: 0;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_modified {
  margin-right: 7px;
  margin-left: 7px;
}
[dir="rtl"] .item_modified.pull-right {
  float: left !important;
  float: left;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
[dir="rtl"] .item_buttons.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .item_buttons .kernel-name {
  margin-left: 7px;
  float: right;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
.sort_button {
  display: inline-block;
  padding-left: 7px;
}
[dir="rtl"] .sort_button.pull-right {
  float: left !important;
  float: left;
}
#tree-selector {
  padding-right: 0px;
}
#button-select-all {
  min-width: 50px;
}
[dir="rtl"] #button-select-all.btn {
  float: right ;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
  margin-top: 2px;
  height: 16px;
}
[dir="rtl"] #select-all.pull-left {
  float: right !important;
  float: right;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.fa-pull-left {
  margin-right: .3em;
}
.folder_icon:before.fa-pull-right {
  margin-left: .3em;
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.fa-pull-left {
  margin-right: .3em;
}
.file_icon:before.fa-pull-right {
  margin-left: .3em;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
#new-menu .dropdown-header {
  font-size: 10px;
  border-bottom: 1px solid #e5e5e5;
  padding: 0 0 3px;
  margin: -3px 20px 0;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.move-button {
  display: none;
}
.download-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
.CodeMirror-dialog {
  background-color: #fff;
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI escape sequences */
/* The color values are a mix of
   http://www.xcolors.net/dl/baskerville-ivorylight and
   http://www.xcolors.net/dl/euphrasia */
.ansi-black-fg {
  color: #3E424D;
}
.ansi-black-bg {
  background-color: #3E424D;
}
.ansi-black-intense-fg {
  color: #282C36;
}
.ansi-black-intense-bg {
  background-color: #282C36;
}
.ansi-red-fg {
  color: #E75C58;
}
.ansi-red-bg {
  background-color: #E75C58;
}
.ansi-red-intense-fg {
  color: #B22B31;
}
.ansi-red-intense-bg {
  background-color: #B22B31;
}
.ansi-green-fg {
  color: #00A250;
}
.ansi-green-bg {
  background-color: #00A250;
}
.ansi-green-intense-fg {
  color: #007427;
}
.ansi-green-intense-bg {
  background-color: #007427;
}
.ansi-yellow-fg {
  color: #DDB62B;
}
.ansi-yellow-bg {
  background-color: #DDB62B;
}
.ansi-yellow-intense-fg {
  color: #B27D12;
}
.ansi-yellow-intense-bg {
  background-color: #B27D12;
}
.ansi-blue-fg {
  color: #208FFB;
}
.ansi-blue-bg {
  background-color: #208FFB;
}
.ansi-blue-intense-fg {
  color: #0065CA;
}
.ansi-blue-intense-bg {
  background-color: #0065CA;
}
.ansi-magenta-fg {
  color: #D160C4;
}
.ansi-magenta-bg {
  background-color: #D160C4;
}
.ansi-magenta-intense-fg {
  color: #A03196;
}
.ansi-magenta-intense-bg {
  background-color: #A03196;
}
.ansi-cyan-fg {
  color: #60C6C8;
}
.ansi-cyan-bg {
  background-color: #60C6C8;
}
.ansi-cyan-intense-fg {
  color: #258F8F;
}
.ansi-cyan-intense-bg {
  background-color: #258F8F;
}
.ansi-white-fg {
  color: #C5C1B4;
}
.ansi-white-bg {
  background-color: #C5C1B4;
}
.ansi-white-intense-fg {
  color: #A1A6B2;
}
.ansi-white-intense-bg {
  background-color: #A1A6B2;
}
.ansi-default-inverse-fg {
  color: #FFFFFF;
}
.ansi-default-inverse-bg {
  background-color: #000000;
}
.ansi-bold {
  font-weight: bold;
}
.ansi-underline {
  text-decoration: underline;
}
/* The following styles are deprecated an will be removed in a future version */
.ansibold {
  font-weight: bold;
}
.ansi-inverse {
  outline: 0.5px dotted;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  position: relative;
  overflow: visible;
}
div.cell:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: transparent;
}
div.cell.jupyter-soft-selected {
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected,
div.cell.selected.jupyter-soft-selected {
  border-color: #ababab;
}
div.cell.selected:before,
div.cell.selected.jupyter-soft-selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #42A5F5;
}
@media print {
  div.cell.selected,
  div.cell.selected.jupyter-soft-selected {
    border-color: transparent;
  }
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
}
.edit_mode div.cell.selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #66BB6A;
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  /* Note that this should set vertical padding only, since CodeMirror assumes
       that horizontal padding will be set on CodeMirror pre */
  padding: 0.4em 0;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. This sets horizontal padding only,
    use .CodeMirror-lines for vertical */
  padding: 0 0.4em;
  border: 0;
  border-radius: 0;
}
.CodeMirror-cursor {
  border-left: 1.4px solid black;
}
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .CodeMirror-cursor {
    border-left: 2px solid black;
  }
}
@media screen and (min-width: 4320px) {
  .CodeMirror-cursor {
    border-left: 4px solid black;
  }
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
div.output_area .mglyph > img {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 1px 0 1px 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul:not(.list-inline),
.rendered_html ol:not(.list-inline) {
  padding-left: 2em;
}
.rendered_html ul {
  list-style: disc;
}
.rendered_html ul ul {
  list-style: square;
  margin-top: 0;
}
.rendered_html ul ul ul {
  list-style: circle;
}
.rendered_html ol {
  list-style: decimal;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin-top: 0;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
  padding: 0px;
  background-color: #fff;
}
.rendered_html code {
  background-color: #eff0f1;
}
.rendered_html p code {
  padding: 1px 5px;
}
.rendered_html pre code {
  background-color: #fff;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  color: #000;
  font-size: 100%;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: none;
  border-collapse: collapse;
  border-spacing: 0;
  color: black;
  font-size: 12px;
  table-layout: fixed;
}
.rendered_html thead {
  border-bottom: 1px solid black;
  vertical-align: bottom;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  text-align: right;
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html tbody tr:nth-child(odd) {
  background: #f5f5f5;
}
.rendered_html tbody tr:hover {
  background: rgba(66, 165, 245, 0.2);
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
.rendered_html .alert {
  margin-bottom: initial;
}
.rendered_html * + .alert {
  margin-top: 1em;
}
[dir="rtl"] .rendered_html p {
  text-align: right;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.rendered .rendered_html tr,
.text_cell.rendered .rendered_html th,
.text_cell.rendered .rendered_html td {
  max-width: none;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.text_cell .dropzone .input_area {
  border: 2px dashed #bababa;
  margin: -1px;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
.jupyter-keybindings {
  padding: 1px;
  line-height: 24px;
  border-bottom: 1px solid gray;
}
.jupyter-keybindings input {
  margin: 0;
  padding: 0;
  border: none;
}
.jupyter-keybindings i {
  padding: 6px;
}
.well code {
  background-color: #ffffff;
  border-color: #ababab;
  border-width: 1px;
  border-style: solid;
  padding: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.tags_button_container {
  width: 100%;
  display: flex;
}
.tag-container {
  display: flex;
  flex-direction: row;
  flex-grow: 1;
  overflow: hidden;
  position: relative;
}
.tag-container > * {
  margin: 0 4px;
}
.remove-tag-btn {
  margin-left: 4px;
}
.tags-input {
  display: flex;
}
.cell-tag:last-child:after {
  content: "";
  position: absolute;
  right: 0;
  width: 40px;
  height: 100%;
  /* Fade to background color of cell toolbar */
  background: linear-gradient(to right, rgba(0, 0, 0, 0), #EEE);
}
.tags-input > * {
  margin-left: 4px;
}
.cell-tag,
.tags-input input,
.tags-input button {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  box-shadow: none;
  width: inherit;
  font-size: inherit;
  height: 22px;
  line-height: 22px;
  padding: 0px 4px;
  display: inline-block;
}
.cell-tag:focus,
.tags-input input:focus,
.tags-input button:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.cell-tag::-moz-placeholder,
.tags-input input::-moz-placeholder,
.tags-input button::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.cell-tag:-ms-input-placeholder,
.tags-input input:-ms-input-placeholder,
.tags-input button:-ms-input-placeholder {
  color: #999;
}
.cell-tag::-webkit-input-placeholder,
.tags-input input::-webkit-input-placeholder,
.tags-input button::-webkit-input-placeholder {
  color: #999;
}
.cell-tag::-ms-expand,
.tags-input input::-ms-expand,
.tags-input button::-ms-expand {
  border: 0;
  background-color: transparent;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
.cell-tag[readonly],
.tags-input input[readonly],
.tags-input button[readonly],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  background-color: #eeeeee;
  opacity: 1;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  cursor: not-allowed;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button {
  height: auto;
}
select.cell-tag,
select.tags-input input,
select.tags-input button {
  height: 30px;
  line-height: 30px;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button,
select[multiple].cell-tag,
select[multiple].tags-input input,
select[multiple].tags-input button {
  height: auto;
}
.cell-tag,
.tags-input button {
  padding: 0px 4px;
}
.cell-tag {
  background-color: #fff;
  white-space: nowrap;
}
.tags-input input[type=text]:focus {
  outline: none;
  box-shadow: none;
  border-color: #ccc;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
[dir="rtl"] #kernel_logo_widget {
  float: left !important;
  float: left;
}
.modal .modal-body .move-path {
  display: flex;
  flex-direction: row;
  justify-content: space;
  align-items: center;
}
.modal .modal-body .move-path .server-root {
  padding-right: 20px;
}
.modal .modal-body .move-path .path-input {
  flex: 1;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
[dir="rtl"] #menubar .navbar-toggle {
  float: right;
}
[dir="rtl"] #menubar .navbar-collapse {
  clear: right;
}
[dir="rtl"] #menubar .navbar-nav {
  float: right;
}
[dir="rtl"] #menubar .nav {
  padding-right: 0px;
}
[dir="rtl"] #menubar .navbar-nav > li {
  float: right;
}
[dir="rtl"] #menubar .navbar-right {
  float: left !important;
}
[dir="rtl"] ul.dropdown-menu {
  text-align: right;
  left: auto;
}
[dir="rtl"] ul#new-menu.dropdown-menu {
  right: auto;
  left: 0;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
[dir="rtl"] i.menu-icon.pull-right {
  float: left !important;
  float: left;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
[dir="rtl"] ul#help_menu li a {
  padding-left: 2.2em;
}
[dir="rtl"] ul#help_menu li a i {
  margin-right: 0;
  margin-left: -1.2em;
}
[dir="rtl"] ul#help_menu li a i.pull-right {
  float: left !important;
  float: left;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
[dir="rtl"] .dropdown-submenu > .dropdown-menu {
  right: 100%;
  margin-right: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.fa-pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.fa-pull-right {
  margin-left: .3em;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
[dir="rtl"] .dropdown-submenu > a:after {
  float: left;
  content: "\f0d9";
  margin-right: 0;
  margin-left: -10px;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
[dir="rtl"] #notification_area {
  float: left !important;
  float: left;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] .indicator_area {
  float: left !important;
  float: left;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
[dir="rtl"] #kernel_indicator {
  float: left !important;
  float: left;
  border-left: 0;
  border-right: 1px solid;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] #modal_indicator {
  float: left !important;
  float: left;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  height: 30px;
  margin-top: 4px;
  display: flex;
  justify-content: flex-start;
  align-items: baseline;
  width: 50%;
  flex: 1;
}
span.save_widget span.filename {
  height: 100%;
  line-height: 1em;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  text-overflow: ellipsis;
  overflow: hidden;
  white-space: nowrap;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
[dir="rtl"] span.save_widget.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] span.save_widget span.filename {
  margin-left: 0;
  margin-right: 16px;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
  white-space: nowrap;
  padding: 0 5px;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
    padding: 0 0 0 5px;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
.toolbar-btn-label {
  margin-left: 6px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
[dir="rtl"] .btn-group > .btn,
.btn-group-vertical > .btn {
  float: right;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
[dir="rtl"] ul.typeahead-list i {
  margin-left: 0;
  margin-right: -10px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
ul.typeahead-list  > li > a.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .typeahead-list {
  text-align: right;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  min-width: 20px;
  color: transparent;
}
[dir="rtl"] .no-shortcut.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .command-shortcut.pull-right {
  float: left !important;
  float: left;
}
.command-shortcut:before {
  content: "(command mode)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
[dir="rtl"] .edit-shortcut.pull-right {
  float: left !important;
  float: left;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
[dir="ltr"] #find-and-replace .input-group-btn + .form-control {
  border-left: none;
}
[dir="rtl"] #find-and-replace .input-group-btn + .form-control {
  border-right: none;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/latest.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Wine-Analysis">Wine Analysis<a class="anchor-link" href="#Wine-Analysis">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Aron-Sun-and-Jordan-Foster">Aron Sun and Jordan Foster<a class="anchor-link" href="#Aron-Sun-and-Jordan-Foster">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="CMSC320">CMSC320<a class="anchor-link" href="#CMSC320">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Introduction">Introduction<a class="anchor-link" href="#Introduction">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Today, the mention of a wine is almost synonomus to its quality. In this regard, the question we wanted answered was is there some wines that are inheriently better than other wines? One way to judge the quality of wine is by setiment. Often setiment is generated by the consumer in the form of reivews on the internet. However, wine setiment is not only exclusive to the consumer but also to a small group of professional wine tasters. These professional are often critizced for rating wines randomly with no ryme or reason. So we wanted to answer the age old quesiton, do professional wine tasters really know what they are doing?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Data-Collection">Data Collection<a class="anchor-link" href="#Data-Collection">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>There are alot of professional wine tasters, and thier reivews of wines can be found on many websites. However, we also found a precomplied dataset of professional wine reviews on kaggle.com that we decieded to use.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="o">!</span>pip install spacy
<span class="o">!</span>pip install nltk
<span class="kn">import</span> <span class="nn">spacy</span>
<span class="kn">import</span> <span class="nn">nltk</span>
<span class="n">nltk</span><span class="o">.</span><span class="n">download</span><span class="p">(</span><span class="s1">&#39;punkt&#39;</span><span class="p">)</span>
<span class="kn">from</span> <span class="nn">nltk.corpus</span> <span class="kn">import</span> <span class="n">stopwords</span>
<span class="n">nltk</span><span class="o">.</span><span class="n">download</span><span class="p">(</span><span class="s1">&#39;stopwords&#39;</span><span class="p">)</span>
<span class="n">nltk</span><span class="o">.</span><span class="n">download</span><span class="p">(</span><span class="s1">&#39;wordnet&#39;</span><span class="p">)</span>
<span class="n">nltk</span><span class="o">.</span><span class="n">download</span><span class="p">(</span><span class="s1">&#39;averaged_perceptron_tagger&#39;</span><span class="p">)</span>
<span class="kn">from</span> <span class="nn">nltk.tag</span> <span class="kn">import</span> <span class="n">pos_tag</span>
<span class="kn">from</span> <span class="nn">nltk.corpus</span> <span class="kn">import</span> <span class="n">twitter_samples</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="kn">import</span> <span class="nn">string</span>
<span class="kn">from</span> <span class="nn">scipy</span> <span class="kn">import</span> <span class="n">stats</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">import</span> <span class="nn">statsmodels.api</span> <span class="k">as</span> <span class="nn">sm</span>
<span class="kn">import</span> <span class="nn">statsmodels.formula.api</span> <span class="k">as</span> <span class="nn">smf</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">accuracy_score</span>
<span class="kn">from</span> <span class="nn">sklearn</span> <span class="kn">import</span> <span class="n">linear_model</span>
<span class="kn">from</span> <span class="nn">sklearn.ensemble</span> <span class="kn">import</span> <span class="n">RandomForestClassifier</span>
<span class="kn">from</span> <span class="nn">sklearn.discriminant_analysis</span> <span class="kn">import</span> <span class="n">LinearDiscriminantAnalysis</span>
<span class="kn">from</span> <span class="nn">sklearn.neighbors</span> <span class="kn">import</span> <span class="n">KNeighborsClassifier</span>
<span class="kn">from</span> <span class="nn">sklearn</span> <span class="kn">import</span> <span class="n">tree</span>
<span class="kn">from</span> <span class="nn">sklearn.svm</span> <span class="kn">import</span> <span class="n">LinearSVC</span>
<span class="kn">from</span> <span class="nn">sklearn.pipeline</span> <span class="kn">import</span> <span class="n">make_pipeline</span>
<span class="kn">from</span> <span class="nn">sklearn.preprocessing</span> <span class="kn">import</span> <span class="n">StandardScaler</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">cross_val_score</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Requirement already satisfied: spacy in /opt/conda/lib/python3.8/site-packages (2.3.5)
Requirement already satisfied: setuptools in /opt/conda/lib/python3.8/site-packages (from spacy) (49.6.0.post20200814)
Requirement already satisfied: catalogue&lt;1.1.0,&gt;=0.0.7 in /opt/conda/lib/python3.8/site-packages (from spacy) (1.0.0)
Requirement already satisfied: srsly&lt;1.1.0,&gt;=1.0.2 in /opt/conda/lib/python3.8/site-packages (from spacy) (1.0.5)
Requirement already satisfied: thinc&lt;7.5.0,&gt;=7.4.1 in /opt/conda/lib/python3.8/site-packages (from spacy) (7.4.5)
Requirement already satisfied: requests&lt;3.0.0,&gt;=2.13.0 in /opt/conda/lib/python3.8/site-packages (from spacy) (2.24.0)
Requirement already satisfied: cymem&lt;2.1.0,&gt;=2.0.2 in /opt/conda/lib/python3.8/site-packages (from spacy) (2.0.5)
Requirement already satisfied: tqdm&lt;5.0.0,&gt;=4.38.0 in /opt/conda/lib/python3.8/site-packages (from spacy) (4.48.2)
Requirement already satisfied: murmurhash&lt;1.1.0,&gt;=0.28.0 in /opt/conda/lib/python3.8/site-packages (from spacy) (1.0.5)
Requirement already satisfied: blis&lt;0.8.0,&gt;=0.4.0 in /opt/conda/lib/python3.8/site-packages (from spacy) (0.7.4)
Requirement already satisfied: wasabi&lt;1.1.0,&gt;=0.4.0 in /opt/conda/lib/python3.8/site-packages (from spacy) (0.8.0)
Requirement already satisfied: preshed&lt;3.1.0,&gt;=3.0.2 in /opt/conda/lib/python3.8/site-packages (from spacy) (3.0.5)
Requirement already satisfied: plac&lt;1.2.0,&gt;=0.9.6 in /opt/conda/lib/python3.8/site-packages (from spacy) (1.1.3)
Requirement already satisfied: numpy&gt;=1.15.0 in /opt/conda/lib/python3.8/site-packages (from spacy) (1.19.1)
Requirement already satisfied: urllib3!=1.25.0,!=1.25.1,&lt;1.26,&gt;=1.21.1 in /opt/conda/lib/python3.8/site-packages (from requests&lt;3.0.0,&gt;=2.13.0-&gt;spacy) (1.25.10)
Requirement already satisfied: certifi&gt;=2017.4.17 in /opt/conda/lib/python3.8/site-packages (from requests&lt;3.0.0,&gt;=2.13.0-&gt;spacy) (2020.6.20)
Requirement already satisfied: chardet&lt;4,&gt;=3.0.2 in /opt/conda/lib/python3.8/site-packages (from requests&lt;3.0.0,&gt;=2.13.0-&gt;spacy) (3.0.4)
Requirement already satisfied: idna&lt;3,&gt;=2.5 in /opt/conda/lib/python3.8/site-packages (from requests&lt;3.0.0,&gt;=2.13.0-&gt;spacy) (2.10)
Requirement already satisfied: nltk in /opt/conda/lib/python3.8/site-packages (3.5)
Requirement already satisfied: tqdm in /opt/conda/lib/python3.8/site-packages (from nltk) (4.48.2)
Requirement already satisfied: regex in /opt/conda/lib/python3.8/site-packages (from nltk) (2020.11.13)
Requirement already satisfied: joblib in /opt/conda/lib/python3.8/site-packages (from nltk) (0.16.0)
Requirement already satisfied: click in /opt/conda/lib/python3.8/site-packages (from nltk) (7.1.2)
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>[nltk_data] Downloading package punkt to /home/jovyan/nltk_data...
[nltk_data]   Package punkt is already up-to-date!
[nltk_data] Downloading package stopwords to /home/jovyan/nltk_data...
[nltk_data]   Package stopwords is already up-to-date!
[nltk_data] Downloading package wordnet to /home/jovyan/nltk_data...
[nltk_data]   Package wordnet is already up-to-date!
[nltk_data] Downloading package averaged_perceptron_tagger to
[nltk_data]     /home/jovyan/nltk_data...
[nltk_data]   Package averaged_perceptron_tagger is already up-to-
[nltk_data]       date!
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># raw data</span>
<span class="n">wine_df</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s2">&quot;wine.csv&quot;</span><span class="p">)</span>
<span class="n">reviews</span> <span class="o">=</span> <span class="n">wine_df</span>
<span class="n">reviews</span> <span class="o">=</span> <span class="n">reviews</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span> <span class="s1">&#39;description&#39;</span><span class="p">,</span> <span class="s1">&#39;designation&#39;</span><span class="p">,</span> <span class="s1">&#39;region_2&#39;</span><span class="p">,</span> \
                        <span class="s1">&#39;taster_twitter_handle&#39;</span><span class="p">,</span> <span class="s1">&#39;title&#39;</span><span class="p">],</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="c1"># reviews = wine_df.sample(20000).reset_index()</span>
<span class="n">wine_df</span> <span class="o">=</span> <span class="n">wine_df</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;Unnamed: 0&#39;</span><span class="p">,</span> <span class="s1">&#39;description&#39;</span><span class="p">,</span> <span class="s1">&#39;designation&#39;</span><span class="p">,</span> <span class="s1">&#39;region_2&#39;</span><span class="p">,</span> \
                        <span class="s1">&#39;taster_twitter_handle&#39;</span><span class="p">,</span> <span class="s1">&#39;title&#39;</span><span class="p">],</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">wine_df</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[2]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>country</th>
      <th>points</th>
      <th>price</th>
      <th>province</th>
      <th>region_1</th>
      <th>taster_name</th>
      <th>variety</th>
      <th>winery</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Italy</td>
      <td>87</td>
      <td>NaN</td>
      <td>Sicily &amp; Sardinia</td>
      <td>Etna</td>
      <td>Kerin O’Keefe</td>
      <td>White Blend</td>
      <td>Nicosia</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Portugal</td>
      <td>87</td>
      <td>15.0</td>
      <td>Douro</td>
      <td>NaN</td>
      <td>Roger Voss</td>
      <td>Portuguese Red</td>
      <td>Quinta dos Avidagos</td>
    </tr>
    <tr>
      <th>2</th>
      <td>US</td>
      <td>87</td>
      <td>14.0</td>
      <td>Oregon</td>
      <td>Willamette Valley</td>
      <td>Paul Gregutt</td>
      <td>Pinot Gris</td>
      <td>Rainstorm</td>
    </tr>
    <tr>
      <th>3</th>
      <td>US</td>
      <td>87</td>
      <td>13.0</td>
      <td>Michigan</td>
      <td>Lake Michigan Shore</td>
      <td>Alexander Peartree</td>
      <td>Riesling</td>
      <td>St. Julian</td>
    </tr>
    <tr>
      <th>4</th>
      <td>US</td>
      <td>87</td>
      <td>65.0</td>
      <td>Oregon</td>
      <td>Willamette Valley</td>
      <td>Paul Gregutt</td>
      <td>Pinot Noir</td>
      <td>Sweet Cheeks</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Data-Cleanup">Data Cleanup<a class="anchor-link" href="#Data-Cleanup">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Numerical values are given to the columns with non-numerical values ('country', 'variety', 'province', 'region_1', 'variety', 'winery') in order for them to be used in the prediction of a wines score (points).</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># assign numerical values to string columns</span>
<span class="n">str_cols</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;country&#39;</span><span class="p">,</span> <span class="s1">&#39;variety&#39;</span><span class="p">,</span> <span class="s1">&#39;province&#39;</span><span class="p">,</span> <span class="s1">&#39;region_1&#39;</span><span class="p">,</span> <span class="s1">&#39;variety&#39;</span><span class="p">,</span> <span class="s1">&#39;winery&#39;</span><span class="p">,</span> <span class="s1">&#39;taster_name&#39;</span><span class="p">]</span>

<span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="n">str_cols</span><span class="p">:</span>
    <span class="n">wine_df</span><span class="p">[</span><span class="n">col</span><span class="p">]</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">factorize</span><span class="p">(</span><span class="n">wine_df</span><span class="p">[</span><span class="n">col</span><span class="p">])[</span><span class="mi">0</span><span class="p">]</span>

<span class="n">wine_df</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[3]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>country</th>
      <th>points</th>
      <th>price</th>
      <th>province</th>
      <th>region_1</th>
      <th>taster_name</th>
      <th>variety</th>
      <th>winery</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>87</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>87</td>
      <td>15.0</td>
      <td>1</td>
      <td>-1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>87</td>
      <td>14.0</td>
      <td>2</td>
      <td>1</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2</td>
      <td>87</td>
      <td>13.0</td>
      <td>3</td>
      <td>2</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2</td>
      <td>87</td>
      <td>65.0</td>
      <td>2</td>
      <td>1</td>
      <td>2</td>
      <td>4</td>
      <td>4</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>129966</th>
      <td>5</td>
      <td>90</td>
      <td>28.0</td>
      <td>8</td>
      <td>-1</td>
      <td>5</td>
      <td>3</td>
      <td>5244</td>
    </tr>
    <tr>
      <th>129967</th>
      <td>2</td>
      <td>90</td>
      <td>75.0</td>
      <td>2</td>
      <td>13</td>
      <td>2</td>
      <td>4</td>
      <td>7639</td>
    </tr>
    <tr>
      <th>129968</th>
      <td>4</td>
      <td>90</td>
      <td>30.0</td>
      <td>5</td>
      <td>5</td>
      <td>1</td>
      <td>7</td>
      <td>10215</td>
    </tr>
    <tr>
      <th>129969</th>
      <td>4</td>
      <td>90</td>
      <td>32.0</td>
      <td>5</td>
      <td>5</td>
      <td>1</td>
      <td>2</td>
      <td>5348</td>
    </tr>
    <tr>
      <th>129970</th>
      <td>4</td>
      <td>90</td>
      <td>21.0</td>
      <td>5</td>
      <td>5</td>
      <td>1</td>
      <td>7</td>
      <td>2777</td>
    </tr>
  </tbody>
</table>
<p>129971 rows × 8 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Data-Exploration">Data Exploration<a class="anchor-link" href="#Data-Exploration">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Before we get into the data analysis let's get a general overivew of some wine trends and relationships that we should be aware of. We first want to get a good understanding of the spread of the data. Data visualization will help us highlight the relationship between trends in the dataset that we might have otherwise missed just by look at the dataframe.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Summary-of-Data">Summary of Data<a class="anchor-link" href="#Summary-of-Data">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>First and foremost, lets get a summary of the rows and columns we will be dealing with. This includes what the data type, number of missing values, unique values the value, and the type of value we are dealing with. This allows us to get a good summary of each column in the wine dataframe.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>From the summary table, we can see many of these variables are categorical. In addtion, we can see that region 1, price, and taster name have a lot of missing values. One interesting finding from this summary table we would otherwise have not known is that there are only 19 unique wine tasters in this data. This means that 19 names tasted around 130,000 wines, which is pretty impressive!</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">summary_table</span><span class="p">(</span><span class="n">df</span><span class="p">):</span>
    <span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;Dataset Shape: </span><span class="si">{</span><span class="n">df</span><span class="o">.</span><span class="n">shape</span><span class="si">}</span><span class="s2">&quot;</span><span class="p">)</span>
    <span class="n">summary</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">df</span><span class="o">.</span><span class="n">dtypes</span><span class="p">,</span><span class="n">columns</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;dtypes&#39;</span><span class="p">])</span>
    <span class="n">summary</span> <span class="o">=</span> <span class="n">summary</span><span class="o">.</span><span class="n">reset_index</span><span class="p">()</span>
    <span class="n">summary</span><span class="p">[</span><span class="s1">&#39;Name&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">summary</span><span class="p">[</span><span class="s1">&#39;index&#39;</span><span class="p">]</span>
    <span class="n">summary</span> <span class="o">=</span> <span class="n">summary</span><span class="p">[[</span><span class="s1">&#39;Name&#39;</span><span class="p">,</span><span class="s1">&#39;dtypes&#39;</span><span class="p">]]</span>
    <span class="n">summary</span><span class="p">[</span><span class="s1">&#39;Missing&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span><span class="o">.</span><span class="n">values</span>    
    <span class="n">summary</span><span class="p">[</span><span class="s1">&#39;Uniques&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">nunique</span><span class="p">()</span><span class="o">.</span><span class="n">values</span>
    <span class="n">summary</span><span class="p">[</span><span class="s1">&#39;First Value&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">values</span>
    <span class="n">summary</span><span class="p">[</span><span class="s1">&#39;Second Value&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">values</span>
    <span class="n">summary</span><span class="p">[</span><span class="s1">&#39;Third Value&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">values</span>
    <span class="k">return</span> <span class="n">summary</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">summary_table</span><span class="p">(</span><span class="n">reviews</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Dataset Shape: (129971, 8)
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt output_prompt">Out[5]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>dtypes</th>
      <th>Missing</th>
      <th>Uniques</th>
      <th>First Value</th>
      <th>Second Value</th>
      <th>Third Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>country</td>
      <td>object</td>
      <td>63</td>
      <td>43</td>
      <td>Italy</td>
      <td>Portugal</td>
      <td>US</td>
    </tr>
    <tr>
      <th>1</th>
      <td>points</td>
      <td>int64</td>
      <td>0</td>
      <td>21</td>
      <td>87</td>
      <td>87</td>
      <td>87</td>
    </tr>
    <tr>
      <th>2</th>
      <td>price</td>
      <td>float64</td>
      <td>8996</td>
      <td>390</td>
      <td>NaN</td>
      <td>15</td>
      <td>14</td>
    </tr>
    <tr>
      <th>3</th>
      <td>province</td>
      <td>object</td>
      <td>63</td>
      <td>425</td>
      <td>Sicily &amp; Sardinia</td>
      <td>Douro</td>
      <td>Oregon</td>
    </tr>
    <tr>
      <th>4</th>
      <td>region_1</td>
      <td>object</td>
      <td>21247</td>
      <td>1229</td>
      <td>Etna</td>
      <td>NaN</td>
      <td>Willamette Valley</td>
    </tr>
    <tr>
      <th>5</th>
      <td>taster_name</td>
      <td>object</td>
      <td>26244</td>
      <td>19</td>
      <td>Kerin O’Keefe</td>
      <td>Roger Voss</td>
      <td>Paul Gregutt</td>
    </tr>
    <tr>
      <th>6</th>
      <td>variety</td>
      <td>object</td>
      <td>1</td>
      <td>707</td>
      <td>White Blend</td>
      <td>Portuguese Red</td>
      <td>Pinot Gris</td>
    </tr>
    <tr>
      <th>7</th>
      <td>winery</td>
      <td>object</td>
      <td>0</td>
      <td>16757</td>
      <td>Nicosia</td>
      <td>Quinta dos Avidagos</td>
      <td>Rainstorm</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Distribution-of-Points-and-Price">Distribution of Points and Price<a class="anchor-link" href="#Distribution-of-Points-and-Price">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>As we mentioned before, most of the columns are categorical varibles. However, there are 2 quantitative columns, which are points and price. Here we just perform a simple description of basic stats on these two columns. From this, one intersting thing that we can see is the points only range from 80 to 100, which is a pretty small range given the number of rows in the dataset.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">reviews</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[6]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>points</th>
      <th>price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>129971.000000</td>
      <td>120975.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>88.447138</td>
      <td>35.363389</td>
    </tr>
    <tr>
      <th>std</th>
      <td>3.039730</td>
      <td>41.022218</td>
    </tr>
    <tr>
      <th>min</th>
      <td>80.000000</td>
      <td>4.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>86.000000</td>
      <td>17.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>88.000000</td>
      <td>25.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>91.000000</td>
      <td>42.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>100.000000</td>
      <td>3300.000000</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Graph-of-Point-Distribution">Graph of Point Distribution<a class="anchor-link" href="#Graph-of-Point-Distribution">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The histogram below further shows how the points ranging from 80 to 100, which was mentioned above, is ditributed. As you can see, the point distribution is almost normal. This is pretty insightful because it suggests that these wine tasters cluster thier reviews towards the middle, rarely giving really low or high points. Next to the histogram, is a cummlative distribution of points, which reinforces the idea that most points are clusted in the middle.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">16</span><span class="p">,</span><span class="mi">5</span><span class="p">))</span>

<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">,</span><span class="mi">1</span><span class="p">)</span>
<span class="n">g</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">countplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;points&#39;</span><span class="p">,</span> <span class="n">data</span><span class="o">=</span><span class="n">reviews</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;#1f77b4&#39;</span><span class="p">)</span>
<span class="n">g</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s2">&quot;Distribution of Points&quot;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">20</span><span class="p">)</span> 
<span class="n">g</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s2">&quot;Points&quot;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">15</span><span class="p">)</span> 
<span class="n">g</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s2">&quot;Count&quot;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">15</span><span class="p">)</span> 

<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">,</span><span class="mi">2</span><span class="p">)</span>  
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="n">reviews</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">]),</span> <span class="n">np</span><span class="o">.</span><span class="n">sort</span><span class="p">(</span><span class="n">reviews</span><span class="o">.</span><span class="n">points</span><span class="o">.</span><span class="n">values</span><span class="p">),</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;#1f77b4&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Index&#39;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">15</span><span class="p">)</span>  
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Points&#39;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">15</span><span class="p">)</span>  
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s2">&quot;Cummlative Points Distribuition&quot;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">20</span><span class="p">)</span> 

<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Rating-Categories">Rating Categories<a class="anchor-link" href="#Rating-Categories">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>This is much like the previous graph, but here we first convert all the points into a categorical varible with a range from 0 to 5 before we plot. By converting the points into a categorical variable, we will later be able to perform some machine learning algorithms on the data. As you can see from the plot, there are barely any points in the 0th and 5th categories.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">points_to_categorical</span><span class="p">(</span><span class="n">points</span><span class="p">):</span>
    <span class="k">if</span> <span class="n">points</span> <span class="ow">in</span> <span class="nb">list</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">80</span><span class="p">,</span><span class="mi">83</span><span class="p">)):</span>
        <span class="k">return</span> <span class="mi">0</span>
    <span class="k">elif</span> <span class="n">points</span> <span class="ow">in</span> <span class="nb">list</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">83</span><span class="p">,</span><span class="mi">87</span><span class="p">)):</span>
        <span class="k">return</span> <span class="mi">1</span>
    <span class="k">elif</span> <span class="n">points</span> <span class="ow">in</span> <span class="nb">list</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">87</span><span class="p">,</span><span class="mi">90</span><span class="p">)):</span>
        <span class="k">return</span> <span class="mi">2</span>
    <span class="k">elif</span> <span class="n">points</span> <span class="ow">in</span> <span class="nb">list</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">90</span><span class="p">,</span><span class="mi">94</span><span class="p">)):</span>
        <span class="k">return</span> <span class="mi">3</span>
    <span class="k">elif</span> <span class="n">points</span> <span class="ow">in</span> <span class="nb">list</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">94</span><span class="p">,</span><span class="mi">98</span><span class="p">)):</span>
        <span class="k">return</span> <span class="mi">4</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="k">return</span> <span class="mi">5</span>

<span class="n">reviews</span><span class="p">[</span><span class="s2">&quot;rating_cat&quot;</span><span class="p">]</span> <span class="o">=</span> <span class="n">reviews</span><span class="p">[</span><span class="s2">&quot;points&quot;</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="n">points_to_categorical</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">total</span> <span class="o">=</span> <span class="nb">len</span><span class="p">(</span><span class="n">reviews</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">14</span><span class="p">,</span><span class="mi">6</span><span class="p">))</span>

<span class="n">g</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">countplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;rating_cat&#39;</span><span class="p">,</span>  <span class="n">color</span><span class="o">=</span><span class="s1">&#39;#1f77b4&#39;</span><span class="p">,</span>
                  <span class="n">data</span><span class="o">=</span><span class="n">reviews</span><span class="p">)</span>
<span class="n">g</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s2">&quot;Point as Catigorical Variable Distribution&quot;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">20</span><span class="p">)</span>
<span class="n">g</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s2">&quot;Categories &quot;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">15</span><span class="p">)</span>
<span class="n">g</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s2">&quot;Total Count&quot;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">15</span><span class="p">)</span>

<span class="n">sizes</span><span class="o">=</span><span class="p">[]</span>

<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Price-Distribution">Price Distribution<a class="anchor-link" href="#Price-Distribution">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Below we can see the price distribution for all prices less than 300. As you can see, there are relativly few wines above 100. Most wines are clusted between 0 and 100 with a the peak wine price at around 20 dollars. It is intersting how fast the frequency of wines drop off, signaling a very saturated wine market for wines less than 100 dollars.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">12</span><span class="p">,</span><span class="mi">5</span><span class="p">))</span>

<span class="n">g</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">kdeplot</span><span class="p">(</span><span class="n">reviews</span><span class="o">.</span><span class="n">query</span><span class="p">(</span><span class="s1">&#39;price &lt; 300&#39;</span><span class="p">)</span><span class="o">.</span><span class="n">price</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;#1f77b4&#39;</span><span class="p">)</span>
<span class="n">g</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s2">&quot;Price Distribuition Filtered 300&quot;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">20</span><span class="p">)</span>
<span class="n">g</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s2">&quot;Prices(US)&quot;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">15</span><span class="p">)</span>
<span class="n">g</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s2">&quot;Frequency Distribuition&quot;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">15</span><span class="p">)</span>


<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Scatter-Plot-of-Points-vs-Price-of-Wine">Scatter Plot of Points vs Price of Wine<a class="anchor-link" href="#Scatter-Plot-of-Points-vs-Price-of-Wine">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>So far, we have only been looking at one variable. Argubly one of the most important relationships in this dataset is that of points and price. In essence, we want to start to ask the question of how does price affect the points given by the wine reviewers. For the plots below, we should expect a linear trend where the cheaper the price, the lesser the points awareded, and higher prices being rewareded more points. In addition, we should see high value wines to be closer in the low price and high points quandrant, and we should expect low value wines to be in the high price and low points category. Looking at the scatter and hexplot below for wines with price less than 300, we can that almost all wines follow this trend, but there is a clear but slight skew torwards low price and high points wines. The hexplot shows us that most wines are priced at around 25 dollars and given 87.5 points.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#Scatter Plot</span>
<span class="n">sns</span><span class="o">.</span><span class="n">jointplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;price&#39;</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="s1">&#39;points&#39;</span><span class="p">,</span> <span class="n">data</span><span class="o">=</span><span class="n">reviews</span><span class="p">[</span><span class="n">reviews</span><span class="p">[</span><span class="s1">&#39;price&#39;</span><span class="p">]</span> <span class="o">&lt;</span> <span class="mi">300</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[11]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;seaborn.axisgrid.JointGrid at 0x7f06f04c8670&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># hexplot</span>
<span class="n">sns</span><span class="o">.</span><span class="n">jointplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;price&#39;</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="s1">&#39;points&#39;</span><span class="p">,</span> <span class="n">data</span><span class="o">=</span><span class="n">reviews</span><span class="p">[</span><span class="n">reviews</span><span class="p">[</span><span class="s1">&#39;price&#39;</span><span class="p">]</span> <span class="o">&lt;</span> <span class="mi">300</span><span class="p">],</span> <span class="n">kind</span><span class="o">=</span><span class="s1">&#39;hex&#39;</span><span class="p">,</span> <span class="n">gridsize</span><span class="o">=</span><span class="mi">20</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[12]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;seaborn.axisgrid.JointGrid at 0x7f06efd7ad90&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAbUAAAGoCAYAAADB4nuYAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4yLjIsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy+WH4yJAAAgAElEQVR4nOzdeZgkd33n+fc3IjKzrr4v9SEJXZaRBQi5LXFqjAGPkO3FsDu27LWH8YHsWViwd2YfY/t5hpnxegfbMIfXNo9lYAd7DRgba9FyyJIxNgxjQI2QkITus1vd6q6+u+vKzIjv/hGRVVnZmVmR2V2VlVGf1/MUVRkZ34xfZYn49C8y4hvm7oiIiBRBMOgBiIiIXCgKNRERKQyFmoiIFIZCTURECkOhJiIihRENegArRKd4ikiR2KAHsFpppiYiIoWhUBMRkcJYK4cfL6hPfOP53Ov+9I2XLONIRESkmWZqIiJSGAo1EREpDIWaiIgUhkJNREQKQ6EmIiKFoVATEZHCUKiJiEhhKNRERKQwFGoiIlIYCjURESkMhZqIiBSGQk1ERApDDY2XWafmx2p0LCJy4WmmJiIihaFQExGRwlCoiYhIYSjURESkMBRqIiJSGAo1EREpDIWaiIgUhkJNREQKQ6EmIiKFoVATEZHCUJusAWnXPkuts0REzo9maiIiUhgKNRERKQyFmoiIFIZCTURECkOhJiIihaGzH1eRTjcUbUdnSoqInEszNRERKQyFmoiIFIZCTURECkOhJiIihaFQExGRwlCoiYhIYSjURESkMHSd2pDqdE2brl8TkbVMMzURESkMhZqIiBSGQk1ERApDoSYiIoWhUBMRkcLQ2Y8Fo07/IrKWKdS66CUgRERk8BRqa1iv17q1W1+zPRFZTfSZmoiIFIZmanIOHXYVkWGlmZqIiBSGZmpyXpZzVqfP60SkVwo1WbV0GHTBcgb8cp0AtJxNt3XSknRi7j7oMSw7M7sL2Jpj1a3A0WUeznLS+AdnmMcOGv8g9TP2o+5+83IMZtitiVDLy8z2ufveQY+jXxr/4Azz2EHjH6RhHvtqpBNFRESkMBRqIiJSGAq1xW4f9ADOk8Y/OMM8dtD4B2mYx77q6DM1EREpDM3URESkMBRqIiJSGAo1EREpDIWaiIgUxpoItZtvvtkBfelLX/oqylduBd3/dbQmQu3o0WHtniMicn7W2v5vTYSaiIisDQo1EREpDIWaiIgUhkJNREQKQ6EmIiKFoVATEZHCUKiJiEhhKNRERKQwFGoiIlIYCjURESmMZQs1M/uYmR0xs4ealm02s3vM7Ins+6am537dzJ40s8fM7J92eM2O9SIiIss5U/uvwM0ty94HfMndrwK+lD3GzK4BbgW+L6v5IzML27xm23oRERFYxlBz968Ax1sWvxX4ePbzx4Efb1r+KXefc/dngCeBG9q8bKd6ERGRFf9MbYe7HwLIvm/Plu8G9jetdyBblrf+HGZ2m5ntM7N9k5OTF2TwIiLDYC3v/1bLiSLWZllP9ww6p9j9dnff6+57t23bdj4vJSIyVNby/m+lQ+2wme0EyL4fyZYfAC5uWm8PcLCHehERkRUPtTuBd2Q/vwP4bNPyW82sYmaXAVcB3+yhXkREZFlP6f8k8I/A1WZ2wMx+AfgA8GYzewJ4c/YYd38Y+DTwXeAu4F3uHmev8xEz25u9bNt6ERERgGi5Xtjdf6rDU2/ssP5vA7/dZvkvNv18rFO9iIjIajlRRERE5Lwp1EREpDAUaiIiUhgKNRERKQyFmoiIFIZCTURECkOhJiIihaFQExGRwlCoiYhIYSjURESkMBRqIiJSGAo1EREpDIWaiIgUhkJNREQKQ6EmIiKFoVATEZHCUKiJiEhhKNRERKQwFGoiIlIYCjURESkMhZqIiBSGQk1ERApDoSYiIoWhUBMRkcJQqImISGEo1EREpDCiQWzUzN4LvBMw4E/c/T+b2V8AV2erbAROuvt1bWqfBc4AMVB3970rM2oREVntVjzUzOxa0kC7AagCd5nZ5939J5vW+RBwqsvLvMHdjy7vSEVEZNgM4vDjS4Gvu/u0u9eBfwDe1njSzAz4CeCTAxibiIgMsUGE2kPATWa2xczGgFuAi5uefz1w2N2f6FDvwN1m9i0zu63TRszsNjPbZ2b7JicnL9jgRURWu7W8/1vxUHP3R4DfAe4B7gIeAOpNq/wU3Wdpr3X364G3AO8ys5s6bOd2d9/r7nu3bdt2YQYvIjIE1vL+byBnP7r7R939ene/CTgOPAFgZhHwduAvutQezL4fAe4g/WxORERkMKFmZtuz75eQhlhjZvYm4FF3P9ChbtzM1jV+Bn6Y9HCmiIjIYE7pBz5jZluAGvAudz+RLb+VlkOPZrYL+Ii73wLsAO5IzyUhAj7h7net3LBFRGQ1G0ioufvrOyz/F22WHSQ9mQR3fxp4xbIOTkSkQI5PVQc9hBWljiIiIlIYCrUCcB+OOhGR5aZQG2LuCwHTS9CsdJ2IyEoZ1Ikicp7mw2XRwvRbeh7N6qgTEVlJCrUh0zZcWFhm2TqtQbPcdaBwE1mNNo+XBz2EFaVQGwKth/q6HfnzListZ12nUBQRWUkKtSHSy8dYi8JmBetQsInIAOlEkSHR73kZK10nIjJICjURESkMhZqIiBSGQk1EpMDUJktERGRIKdRERKQwFGoiIlIYuk5tCLj7wvVjPVwE5k1Xba9EHWSXAvR4rVrj97M+tici0kyhtoq5O0lrNxH3JXf87eoC8tW1W7ZcwebuaZPkpro84xQR6UShtkq1C6bm56D9rKZTXeKAO4F1rus2lk7b61hD1jaL9uHW7zhFpDfq/SgD1S3M2q3b2PHnrUs8nQ1BGhrdwqzd9hp1uWtYHG69jNPcMYWbiPRAobZKtB6KyytJvPearCDosxlWv4ckvcexNgJRhyRFJC+d/biKrHS/xZW80WfzyS4iIstFobZKaIcvInL+FGoiIlIYCjURESkMhZqIiBSGQk1ERApDoSYiIoWhUBMRkcIYSKiZ2XvN7CEze9jMfiVb9m/N7AUzuz/7uqVD7c1m9piZPWlm71vZkcswWcnr8ERWq+NTVT7xjefnv4puxTuKmNm1wDuBG4AqcJeZfT57+j+5+we71IbAHwJvBg4A95rZne7+3WUe9rLyflqJsHBBc+K9d7j3Rlv8HjrqNxoVp3U9dPk4z3Tpr/P/4u9qSCKyNgxipvZS4OvuPu3udeAfgLflrL0BeNLdn3b3KvAp4K3LNM4V0QimXnf77k7sMBdDLYG6N1ptdX8l9zQEY9Ka2NNlS+VOY52YtCbOvb0L0UnE5ltm5R1n4z31puUiUnyDCLWHgJvMbIuZjQG3ABdnz73bzL5jZh8zs01tancD+5seH8iWncPMbjOzfWa2b3Jy8kKO/4JoBEKSY0fdWpe4U03SMGtIHKoJ2eu1uYUMWaCRfs3XAbVsebvQaCxrrXPSUExoH255Ai+P5tngfFB1GWe7fyB0qxMpoub935mTxwc9nBW14qHm7o8AvwPcA9wFPADUgQ8DVwDXAYeAD7Upb3cQqe1uyt1vd/e97r5327ZtF2Lo562xo280L+6lG3/jq56ks7NOtXVPw26+hsWzrE6bjD2tpWn9Rkh0q0sW1fmi7+fDzDoe3mydfc1/X+I1NWuTtaJ5/7du4+ZBD2dFDeREEXf/qLtf7+43AceBJ9z9sLvH7p4Af0J6qLHVARZmdQB7gIPLP+ILp/EZWK/d6pPsUGM9R6GTztoahwhjFs+yutXVGocWIXcdNB/KPL/E6BZmzRbNvsj/fjbXiUjxDOTWM2a23d2PmNklwNuBV5vZTnc/lK3yNtLDlK3uBa4ys8uAF4BbgZ9ekUFfAP3uTD07tNirRjj1epJE41Bkr3WN36/fkzL6ub2Mskmku83jZX76xksGPYwVM6j7qX3GzLYANeBd7n7CzP7MzK4j3U89C/wSgJntAj7i7re4e93M3g38DRACH3P3hwfzK4iIyGozkFBz99e3WfazHdY9SHoySePxF4AvLN/oRERkWKmjiIiIFIZCTURECkOhJiIihTGoE0VERGQFNHo/5lGEsyQ1U1tBidNzBxGAeuLU4t47dNQTZ7ae9FyXuFONe69LLw7vfZze5zVuzRelr1RdcoE6pYjI8tBMbQU0OoE0X2oW5rieK3HnbDVhpp4+DgxGIwiD7oXuznQtYTarm67GrB8JKYVL11Xj9Atgru6MlQOiHNuLs4u9Ie1oUg49R11a03hfYococMIl3pi2bcCyZd2udWuum7+mzh2zpa+Ra7Q0a9TmrRORlaVQW0aNpsNxm3/Yx4B5OlVu3S+6O3MxnJ5LFl1cnDhM1ZxS4IxE7TtvVGPnbEtd7HBiJmYkMiYqAUGbunrizNYW1zkwVU2IAhgtta9L3KnFLeMn636SOOWQDnXtu6PUE4hxSkH7wMjTQLmXuka4BXSua9eSbKk6ERkMhdoySbLZWbddcKMVVeDpLAzSIDg9l3StrSVQrzojEfOzrzhxpqrJoibHrWbrzlw9Zl0loJKFYuLpIcq4S109gTNzCSORUQ7TuvnZZ5dfMHaYqUMpWAip1tlZp/elmkBoTmjMby+v5llb3rokS6mgaXt57gjUWicig6VQu8DaHWpcSgIkiTNTc6bzNHck3dnO1J25eoIZ84ca89SdnkuIajBaMuo9DHS2nh6arIRBT+2pakkajOXQSdr2pG6vMcstBd5D1YJ+PvtKskOSvVam97TztrNSkUFaa22ydKLIBZYsMQvpZC4md6A1q3v+QGsWO9TaHRddQnp3gT7qaH8YNnfxCup3c+m9U3USicggKdRWjZXdGWo+sTx0CFJksBRqIiJSGAo1EREpDIWaiIgUhkJNREQKQ6EmIiKFoVATEZHCUKiJiEhhKNQuoMaFt712ck+y5rj1xHu6sNnd8SS9iLrXC6LjJGvj1XMH//466kN64XZfXT7o/c4G7gtfK6Xx++n6a5HBUZusC6Cxo56rOzNZV5AogFKYPt/pgtzGDvDYTMz+kzVih/WVgM1jIdalDrIO/nMJL56tEzusKwdsGwuX7ByfdtR3ZutpK6hKZKyrBEtur9EHMXGI62lPxkrEknUNRksT4PSNWbIOFnpFNv5j7VbWCJRFueJL110QZmkH/2wcug5bZOUp1M5ToxP/dDVZ1AaqnqSzoXJkbTu5x9k90p4+XmWqtlB4ei5hqpqwdTxs2xk/yW7zcvBMjemmujPVhKlawraxkPHyuXWe9TOcrS0e51zdqdZjJsoBI6VOnfGz+8A1j99huuaUQ0t7M6Yp1fY9SoOv+XfIltG9btEYgFp2V4Ow8bpNZW3DjJZlyxhuze/bSmxPJK9ebhK6lGHoIalQ60PzIbTp2sL9x85ZjzQ0QoNy0zudOLxwusbhs3Hbutjh8NmY0Shh20RE4zZoDhybijk6074ucTg8FTMyl7BjPCIM0u7/7iy6T1q7cZ7J7tu2fiRs6oy/MDvrpBqnhzEroRHY4vBuDbPWbbo3jn/nv31Lko0nyqZ+Zt0DrXWbF3oW1XV227S9dN0Ls00R6Uyh1ofY05nWTC1fN/fYYabmJIlTTeD5k9Wut4hpmKk7+0/WWD8SUA6Nw2fruepm685zp2psGQ2YKAdU4/b3BGtVT+D4dMxYyRgrBySeM2g8HWspaByStNw78MasrZdgg7SRs5H+B9zLR1jNs6jzDZk8421sT4ckRVaGQq0P9Xjhs7NenJpLOHSm3vNO+PhM3NMtYhrOzCXzs65ezMVOJel9B1xPYITe6xozml41ZpErHRT9Ni1WoIksP539KCIihaFQExGRwtDhRxGRAtOdr1eAmb3XzB4ys4fN7FeyZb9nZo+a2XfM7A4z29ih9lkze9DM7jezfSs7chERWc1WPNTM7FrgncANwCuAHzWzq4B7gGvd/eXA48Cvd3mZN7j7de6+d9kHLCIiQ2MQM7WXAl9392l3rwP/ALzN3e/OHgN8HdgzgLGJiMgQG0SoPQTcZGZbzGwMuAW4uGWdnwe+2KHegbvN7FtmdlunjZjZbWa2z8z2TU5OXpCBNw8g6OP07FOzMWfm4p77H05VE07O1HuuixPnbDXpuc4d5uq91zW22U9dul01TRS5EJZz/7fa2SB2JGb2C8C7gLPAd4EZd//V7LnfBPYCb/c2gzOzXe5+0My2kx6y/F/d/Svdtrd3717ft+/8P35L3OcvZG70bcxzMfRcPeE7L85y6GwddyiHxkUTEeWo+78p6omz/1SVY9MxWFp38YYyY6Xude5OPUnbdxkQBrB1NKSyxPZaBQbj5YBSuHRdYGTXxKWPS4ER5kz+dp1HlroWzMj+RWa9X+PWWL/f68bytvZq3d75bFOkRe7/ki5/6cv9//ivn1vOsSyyQieldPz9B3L2o7t/FPgogJn9n8CB7Od3AD8KvLFdoGW1B7PvR8zsDtLP5rqG2gUYL/XEFwWYWdo1o2xpL8Z2HajcnedOVnnw8FzaPzFbPhc7z5+qsWEkYMtY1LZP4/GZmGdPVtMLjAE87RTy5LE5No+G7FxXahsaceLUmtqHOOlF0YenYsZKCZtGwtxhk3h6AXcpcMYr5/aThKyrR3DuzrqWpO9ZObSOAWXZV7v/PN07dxhp1/sxj/MPs94Kz3d7ItK7gYSamW3PQukS4O3Aq83sZuDXgH/i7tMd6saBwN3PZD//MPDvl3OscZLOzjrNZ82MMHBC0llbI4pPzcZ86+AMUy2NjhuctHnxmbkqOyYixsvprnqmlvDMySrTtaRtaysHTszGnJyN2bOhzIZKkPVpTMOsUzssJ+1TOV2rs2kkbZ+VdyddS5yTM2n7rEq0UBdaOkPr1t9xLnZCc6JgIdzy7uwb/65p1AV07yfZyXmHWR/FCjSRwRjUdWqfMbMtQA14l7ufMLM/ACrAPdlO7Ovu/stmtgv4iLvfAuwA7siej4BPuPtdyzFAzw41dugBvEhjp1sK0prvvDjLsydrS/ZbbDx/6EydkSi9hczkdDzfSHipuv2nqhyNjD0byksPkoXXPDGbcLbmbB/LP2uDNBTn6jHrR8JsBpavLnZIYqccQmD56xYG7oRmAzrUqDATGSaDOvz4+jbLruyw7kHSk0lw96dJLwNYdvUOhxS7MTMOnKrmCrRmTtoXcjpng+SGxu1gEve2hwa7bQ/6O9kFoBz219+x26yum7DPun5mdfO1fRQq0EQGT22yLrBewqyZ0++O2/pqBpzduaX3Ouuzro+aYaRAExkstckSESkwtckSEREZUgo1EREpDIWaiIgUhkJNREQKQ6EmIiKFoVBbRfptw7nS3Tt11rqIrFYKtQ7CoPeddz1xNo2GPV+r5u4YUIt763BvwGw9od5jHdm2ksTpNRLrSdo6rFfO8IR2v1s9n99RRC4MXafWQWDGSNRozNt9Xfe0qfGDR2b5+v5p6gmMRcZ4jv6KiTvHpmOeO1kjdthQCdg2EebqEFIOYSQKODmbUImMdR2aDjczoBIaG0YC3Ix6AqF1bh7cXFcKYUMPDZEbAoNKlI6t1/CNrP/uHv1cCB1k21uqVdmF2p6IXFgKtS7MjHJoRMHCLWda1WLn5GzM3U+e5fhMPL98uu7MxjHrKwGl4NxO9Yk7c3XnyeNVpmsLL3xqLuFsNWHHRMhY+dyQauw8x0sBUVO4zNWdaj1mXSWgEp27vUbdppFg0S1oHKg7hHi2Tvu69SMBIz3eugbSMAubgslyBlvAQsD0qt+mx7ZonEDOYFOgiaweCrUcAjMqYdoLspo1hIwTJ06cf3humkcn59rWJQ4nZxPKobG+aRYVJ87+UzUOT8Vt62KHg2diRqOEneuiNLyyneZIaG1DCxY6/0e1dEbVCAUDxsvGui4zx0afy4jFs7bRkjGRYwbYKgqgHLbfXmNZu3AzWBSCvTjf2dk5r5e97Z1mbQozkdVHoZaTmRFZusM9cLrG4bN1vvb8NLP1pf8tX42do9MxpcBI3HnuZC3XzUVn6s7TJ2rsWheyaTRkrJQvXOoJHJuO2TASsL5ibBgJF83qutY6lCy9D9q6Skgp7P1QYzkMch2ibJ21pbeyGXyYnfP6LeGmxsUyTI5PVfnEN54f6BhWsk2XQq1HZsbBM3W+8swUOXJpkeMzMcdn4p5PJJmtO+Ol/Pc/a4gT2DQSEvTajt+MjaP5PtdbVEb6GV8v45y/Nxsr24m/n0ObjXATkdVLZz+KiEhhKNRERKQwFGoiIlIYPYeamQVmtn45BiMiInI+cp0oYmafAH4ZiIFvARvM7D+6++8t5+BEROT86Cah7V3j7qeBHwe+AFwC/OyyjUpERKQPeUOtZGYl0lD7rLvXlnFMq95UNaEc9X5y94vHT3Nw8njPraLqSXqdW691gcFsH30h++lD2ZB4+4uqV5t++jS6L3yJyOqU9zq1PwaeBR4AvmJmlwKnlmtQq9VUNeG/75/myNk6G0dC6olzYiae78bRyfRcja8+9AzPHzmFOzx94DAvu+olrBsfXXKbgcHZqjNdq/Hi2TqXbyozXu7+bxEDNowEjJUCpqrOTM1ZVwko57iQeiQyRkKjFkM9diolcl24HRiEZiSeBlsYeK7r3Iz0X1b9trXqm4Ob425LvlYjxLxlmTqKiKw+eUPt/3P33288MLPngZ9fniGtPok73z0yxwMvzqYzEdILd0uhsW3cmKomnKmeeyl24s7Dzx3m64/sz5oep7vFM1Mz/ON3HuXiHVu56tJdRGHYdruN7lhOGhSzdefRo3NsGQ3Zs6HUNmxGImNTy4XTicOp2YRKSMeWV1GQ9pNs7v/owGzNCQOnElnbOmMh9JovZo4TSPD0bgcd9vyN37rXYGj82s2v29PdDVo26Nn/tBtHt8bG3epEZDDyhtpngOsbD9zdzexTwPcvy6hWkcmpOl99bprZWtJ2RmZmTFRCRksBJ2fj+d6Qk6em+Lv7n+LM9Bz1eHHgOeCJ88LhYxyaPM73XXkpO7ZsnH++OataN5k4HMs6k1y6scTm0RAzIzTYPJq2teoUInMxVKcTxsvGSNY/0mg0R+4cPnEC01WnHPqi1w/NunbmcNKWXYH5ovUC+mw63NTR45zGy2bg3rUBsTVepMNYm2dfebv0t9aJyGB1DTUz+17g+0jPdnx701PrgZHlHNigVesJ33xhZv6WMEsJA2PzaMjZuTpfvO8ZHt1/lDhJuu4Y60kCCXzn8WfZvGGCV159GVHUftbWrNFm69mTNSan6ly/c5SNWbgtxYGpqjNbc7ZPhD2136rG6a14xsuW3XkA8jSOahySLAVOmCVTr/v/drOzc2Qh3bZRcs7fsd97ojXqeu1IJrLcVkPvx370e8bmUjO1q4EfBTYCP9a0/Azwzr62OCQeO1blmRO13u6pZcajB47y6IFJ6j00eIyThCjqvUdj4jBaClg/ki/QGhyIQmOsj36SBm1vpZNH2n2/57Ke+zQ23wWgn3H2S3kmMnhdQ83dPwt81sxe7e7/eKE2ambvJQ1FA/7E3f+zmW0G/gJ4CelJKT/h7ifa1N4M/BfSj2Q+4u4fuFDjatbrTSIbksSx+U/C8rOsqlcrudOG4dpxr/R7IyKDl/cztSfN7DdIA2e+xt17PlnEzK4lDbQbgCpwl5l9Plv2JXf/gJm9D3gf8GsttSHwh8CbgQPAvWZ2p7t/t9dxiIhI8eQNtc8CXwX+lrSryPl4KfB1d58GMLN/AN4GvBX4wWydjwN/T0uokQbhk+7+dFb7qaxOoSYiIrlDbczdWwOmXw8Bv21mW4AZ4BZgH7DD3Q8BuPshM9vepnY3sL/p8QHgxgs0LhERGXJ5Q+1zZnaLu3/hfDfo7o+Y2e8A9wBnSS/orucsb/chSdsPr8zsNuA2gEsuWTt9z0REWvd/6v14rveSBtuMmZ02szNmdrrfjbr7R939ene/CTgOPAEcNrOdANn3I21KDwAXNz3eAxzssI3b3X2vu+/dtm1bv0MVERk6a3n/lyvU3H2duwfuPuru67PHfd9+pnFo0cwuAd4OfBK4E3hHtso7SD/Ha3UvcJWZXWZmZeDWrE5ERGTpi6/d/VEzu77d8+5+X5/b/Uz2mVoNeJe7nzCzDwCfNrNfAJ4H/lk2hl2kp+7f4u51M3s38Dekp/R/zN0f7nMMHbk73S+b7i7ps+OtM1ynzIuIrDZLfab2v5Eel/1Qm+cc+KF+Nurur2+z7BjwxjbLD5KeTNJ4/AXS298sC3enlsDu9SWeOlZltu65OopAehH1nq3rCIKAxOPcnSmi0DhzdgrDe7rCLTQ4PVvHe4zD+S78uSsWxFmX+n4uASt6aKsXpMjgLXXx9W3Z9zeszHAGxz0Nr0aAra+E3HL1Oh6dnOO7R+bmGxl3qq0nzjeefJEvP3yQGmHWiTgmsIW2Vu2EgXHFrm1ce/luojCgFjuzMUuGW2hw6cYSr9w1SilIx13LcbFFo4P/nvUlotCoJ061ni/eyqGxfiQkDIzEnfjcHs5tBQaVEAKzni9q77WbyPnqtfdja52IDFbeO1+XgH8J3JQt+nvgj4tyX7Ukm521Csy4ZvsIl24sc+8LMxydqp8za6vFMUdOzfCZbz7DsbOzQLYTDiM8CCGpg5/74lEYMDFa4VXXXMbGdWPzy8uREYVONXaqbUIqCtLWWK++eJQtYwt/vsggNKcW03ZmGQBhAJduLDNRCZpezwhL6cyt3iGkAoP1IyGVKGhaZljg830dO6mEjfZYjU7+pLd96VySrpetO4hAg4VxQv6xisjg5T2l/8NACfij7PHPZst+cTkGtVLSGRYsNeEYLwf84GXjvHC6xr0HZqglTj1OqMYJn7vvOR7cf7xtnZnhYQkswZLa/G1dzIzrrtzDFbu3td1pB5Z20Y8CZ7bui7rAv2xHhe/ZWml/GxgzylEa0tX6ws7YgO0TIdsnoi51RpQ4c/XFhyXHSuldCNqNs3F3gCCbtTXXRQblsH0oNbrtd5oNDWp2ds7yxrIO41SYiaw+eUPtB9z9FU2P/87MHliOAa2kPIHWbPf6Eju+N+Ivvn2EBw6c5u4HDzCb45ifBQFuZTaMltg4PsJ1V+1hpFxasi4KjPFSethvvMoiLFgAACAASURBVBzwyl2jjJWWPmE1MKMSpZ/PlcKA3eujRbOsjnWBMVIiu++bsa4SEuW4saiZEQY+H1LlML0tzdJ1i8NttYTZOeu1jNOalovI6pI31GIzu8LdnwIws8s5/3ZZQykKjNmZGb5w/3MdD9e1Y2Zs2biOvVftwizv5YFZ3VjEdTtHCHvo4m9mjJWM3etKPXX/b8zaeu3gn85AodRHJ/5GaKzGQFtU08ctc0RkZeUNtf8d+LKZPZ09fgnwc8syIhERkT7lDbWvAX/Mwin3fwxcsFvRiIjI8lhtNwld7pZdeUPtT4HTwG9lj38K+DOyC6RFRERWg7yhdnXLiSJfLsKJIiIiUix5z1j4tpm9qvHAzG4kPSQpIiKyauSdqd0I/HMzaxyYvQR4xMweBNzdX74soxMREelB3lC7eVlHMUTcnWdP1glKIzA321Pt2ZPHeOqpWa644oqeT18/Nl1n23jU22n2wHQtYbzc2+n5kF6rFga9n2afAIH6H4rIgOQKNXd/brkHMghhAEkP15odPF3lt/72AA8emqUysZ7y6BjTZ06RxN0v2fN6lfj4fvZPn+FgGPDwww/zute9ji1btnStCww2VMJs2zGTUwmXbioxUV76qPFoZIRmnK0607WYDSNBrguwQ0u/EockdqKAXNe5NTXfICYLNvKHWz8Z2FzTa59G6L8xs8gw2TxeXlM3Cc07UyukwIxysLiRcTu1OOFPvzXJ/71vknrc6NpvBGGJsQ1bqM9OMzt99pw6dyc5fYTaiUMEeNqWq55w6uRJvvjFL3LVlVdy/fd/P6XSud1FRkvG+ko439YqAeZi54ljVTaNBOzZUCJqEzalwBiNbNEMK3E4MZNQCZ31I0Hbi7gD0r6SmC0Ki3riWOJEoXWctVn21VzY+LdCmCM4ep0Ntu3okaNPozqBiBTfmg41SHeokUGYNTVu3Sne98IU7797Pydn6sy1dLP3rL4yOkZUGWXm7CniWhWAZG6K+uSzENfAk0XtuByI45gnn3qSp595hle/+tVceuml6VgC2JR1wm+3s3eHkzMJJ2fn2LM+YstY2pcxMBiLgq6tpuZi5+hUzERlcceQKEhDrVOdkzY8DswXjStPSMSAeeP1Fz/Xb5i122ajs37zjDFPnYgUy5oPtQYzoxQ4CWlPyNOzMR/48gt89ZnTzC5xa5YEwwJjbN1G4rlpzjz/XWpnjrHUDdXq9RiI+drXvsaTjz/Gj938JjaMVZbc2ScADgdO1zk2HXPN9grjOdtaOXB2zpmpxWwdCyl3mYGds93skGQpu41M3oBoHJJsnrVdkNlZ6zrZc41wU59GkbVHodbEzAiBIHDueOgYX37qVE/9HTGjdvoY9bPHlwy0ZvV6nQ0TY6wbKfW0s08cKlHAaNTbiSBp82Cj1EOgNRiNxsM9laW1fTYs7rVPY3N3fYWZyNqiUGvDsptZ9hRoGe/x7tUL2wx6CsL5up4rzq9umCjQRFZfm6zzkeeEl/zt4kVERFY5hZqIiBSGQk1ERApDoSYiIoWhUBMRkcLQ2Y8iIgW21tpkaabWhrszU0/6Pu3d+zg1H9A56CIi50mh1mK2nvDY0Tmu3j7G9okSlaiHoKnPEQYh8dSJtD1WTqUo5OCRSeZq9Z4CMTA4W41J+sjQWuwkfRQ6fV1ON18rIrKcdPgxk7hz6Eydw2frOLB9osxvv+VS7nniJHc8eIw48Y5Nj80T4nqVY3//pxy++3Y8rjN25Q+w7pU/Qlgq02nOZ2YEQcD3XH01r3zl9Zyuh1RJWF8J5hsZdxIYXDQRccXmctvGxp0YMFYyNo2GbRsbL7XNStaFxMkfUkba+X8luomIyNo2kFAzs18FfpF0v/gg8HPAx4Grs1U2Aifd/bo2tc8CZ0jbCdbdfe/5juf0bMyzJ6vUWxoah4Fx89WbuPHidXx832EeOTJDtSXZvDrDzKHHef7Pf5Pq0f3zy6ef/Caz+x9m441vp7Tze7BwcSf+UhSxYcN6Xvu617Np06b55bN1Z64es6ESUInObWMVGlQi45ptFdZlt6XJoxEsW8ZDRnLcgqa1thzaohBs1zi4ndBYMqA7bRMUaCLSmxUPNTPbDbwHuMbdZ8zs08Ct7v6TTet8CDjV5WXe4O5Hz3cstdh57lSVM3NJ10N4m8YifuWm3Xzn0BQf++ZhZmoxtVqN+twML3z6tzj1wN1t65K5KY5/5c8ob7+cja/5ScKRCYKoRBCG3HDDDVx55ZXtO/EDJ+cSSjXY2OjYT7qDv3xTid3re+sRacCGkYD1ld5vFhoF6e1s2tU1bjnTbtam2ZmIDMKgDj9GwKiZ1YAx4GDjCUv3gj8B/NByD+LIVI1Ts/kbPL585zi/+yMv4T/8+d3c9617OfS53yeZm1qyrnrkaY7c+btc8WPvZtcrXsf37/0BRkZGlqyrJTA5HbNzImLbeMiVm8u5bvTZ0JjVbRoNezpECemhxnJouWZZrWsozERkUFb8RBF3fwH4IPA8cAg45e7NU53XA4fd/YlOLwHcbWbfMrPbOm3HzG4zs31mtm9ycrLDWHoffzkKuGz6EQ5/9vdyBdq8JGZ8bpJX33hDrkBrFgVw9dZKT4EGUAqNLWP9BVolZ6A1NGZtCjSRwcuz/yuqFQ81M9sEvBW4DNgFjJvZzzSt8lPAJ7u8xGvd/XrgLcC7zOymdiu5++3uvtfd927btu0CjV5EZPVby/u/QZzS/ybgGXefdPca8NfAawDMLALeDvxFp2J3P5h9PwLcAdyw7CMWEZGhMIhQex54lZmNZZ+fvRF4JHvuTcCj7n6gXaGZjZvZusbPwA8DD63AmEVEZAgM4jO1bwB/BdxHejp/ANyePX0rLYcezWyXmX0he7gD+G9m9gDwTeDz7n7XigxcRERWvYGc/eju7wfe32b5v2iz7CBwS/bz08Arlnt8IiJFUZQ7X+ftX6k2WSIiUhgKtR65OwfZxOj3/RDnXqHV3a4rrqFSKi29YouNIyFhH6e7l/r86+rMehEZVmu69+PWsYgTswn1xHM1BX7x1Cx/8HdP8HR4NVve8l423Pg/cfiO/0Bt8pmudRu27+Infv33ufRlNxCVI9zhbDXp2EuyYSQybtwzys51JSJLL9DLM87AYNNoyFipt2vNIO0e0uPlcEB6jVm/YagQFZELZU2H2kgp4NrtFQ6frXPobL1jYNTihM986wB33n+QepK11IoqRNsvY9fP/wFTD3yRY1/6CF6bXVQXhBGv/8l/yZt+7l9TKlewIO3VaAbrKgG1xJmuetsWU1dtKfPKnaNEwcLFzAaEeNdwGy8Zm8fC7GLm/HERZh1E6LEO0hDtp079HUXkQlvToQbpjviidSU2j4U8d7LG2eriPpAPHjjF//V3TzA1V6cat7bUMqxUYd31P8LYNW9g8nMfYubx/w7Apdf+ALf+mw+zfvN2ospo2+2WQ6M04kzVnFo2bds0GvK6S8YYLwftO4FY2gcywHFf6LlYCmDLWEipj04gaTsshZlIEa21m4Su+VBrKIcBV22pcCrr2H9ypsaHv/wU9+8/yVy9e39ID0oEYxvY/rbfwCaf5jWXreOaV7+RUpswa2VmTJQNd+fqrRUu21TO1WrKzDBLP+NbXwlYVwl6np01mhU3Xi+v5pZWCjQRWU0Uai02jIS8bPsIv/O3B9n33HHOmZx1YaURvu+G13Lt9+4mDPPfFgZg1/oSl28q93yPs5EoDbRePzsLrHP3/aWY+juKyCqlsx/bCAJjvBT0FGgNFgQEQe9va79/CIWEiMgChZqIiBSGQk1ERApDn6mJiBTYamyTtZxnY2qmJiIihaFQExGRwlCoiYhIYSjU2nB33L3vnoQ52jO2pbPzRUTOj0KthbsTJ/CjL9vB5VvHGO2h1X0YGAeOTTE1F5N4/mgLDU7PxT2P1WC+vVav8jRGFhEZNjr7MdMIs8a+/pLNY3zuf7mRT9z7Ah/82yepx06tQxKkTUCMbVs2sW3LZh48UmXbeLhkhxDLaq/aUuaabRVCg9ghT74ZMFE2No6GBJa22cobVKUAKlGA9VhHNl51ExEZHur9uAYlWaC1CgPjZ2/cw83XbOP9n3+M//bUcWZri1cMAmN8ZIQ9O3dQLi/cK21yKubEzAyXby6zeSQkaAm3yGD9SMANu0dZXwkXLQ/NqcZQbxM2Rtqzcet4NN9VH9KgCegeUAaMloJFQduoa26O3I7CTESGwZoOtdbZWSfb1lX4o1tfzteeOs6v/b/f5fRsnVrsmBl7LtrB+nXjbXf49QQeP1plXTnge7aWKYdGGBihwSt3jnDphlLbOjOjEkHkzlx9YXwGbBoNmCgHHevCrMlxa7iVw/SuAJ3qrENdI5QUaCIyDNZ0qOUJtGavvWIzX3rPq/lXn32CBw5Ns23rFsIcfR7PVBPuOzjLDXtGuWJjiZfvGFk0y+okNGM0Su+fFpixaTTM1fC4MfuCdIZVifI1PJ6ftQHump2JyPBZ06HWj0op5M3X7uJocmrJO1c3c9Kd/XUXjbS/T1oHZkYltPTWMr3cHsbSe6RVOszOutVlHxH2RYEmIoOksx9FRKQwFGoiIlIYCjURESkMhZqIiBSGQk1ERApDoSYiIoUxkFP6zexXgV8kPdP9QeDngPcB7wQms9V+w92/0Kb2ZuC/ACHwEXf/wIoMOuPu3P/8CY6enGLj+omeTpffPBoyVY1ZXwl7qgssvaYuDLy30/NzrykiRbXSNwkddEuuFQ81M9sNvAe4xt1nzOzTwK3Z0//J3T/YpTYE/hB4M3AAuNfM7nT37/YzljBIu37k9fTRaX7ts4/z+OQUtdiZPHGaiy/ayuhIpWvd+krAW66a4KKJiDNVZ7pWZ/NoSCXqPlFO21oZUWA46VjDwHNdSF0O0+4ivWotyXspngJURFaDQV18HQGjZlYDxoCDwEty1N0APOnuTwOY2aeAtwJ9hZqZEQVpa6huPRNnazF/+JXn+fg3D1KLk/l142qNJ/e/yJYNE+zYuumc7iKBwQ27R7hhzxhRkG7PSXs6Tk7HjEYJG0dDwjYhVQ6Nkcjmx9kQJ5DghEH7bh+hMd+tpNduII21F5X5om/560REBmDFQ83dXzCzDwLPAzPA3e5+t5m9Bni3mf1zYB/wr9z9REv5bmB/0+MDwI3ttmNmtwG3AVxySefpcKNfYtChD+RXnzrBr9/5GGdmY+baTOvcnROnz3Li9BS7d2xhw8QYZsbu9RG3XDXBWDlo20HEgZm6M3OmzsaRgPFSMD+W0VLQtUVVY9YWmM+vZ6Rh1k9rq26hlPaETNdpfW8UZiKrU/P+b+tFuwc8mpW14ieKmNkm0tnVZcAuYNzMfgb4MHAFcB1wCPhQu/I2y9pOItz9dnff6+57t23blmdcRKERZu/I8akqv/Sph3j3X36XybM1Zrscp4wTJ04SXjh8lEOHj/AjV43zP16znvUjYdeWWJ59nZxNODJVpxIa4+W0i36eYEo8DbcogJGo90Az8gVT2tC4Zf0cdSIyGM37v3UbNw96OCtqEGc/vgl4xt0n3b0G/DXwGnc/7O6xuyfAn5Aeamx1ALi46fEe0kOXF0xgRhTAX377Rb765IlzbjXTTZw4L985zpVbypR6+EDLSWdn5ai3Po2QBlopC8G+mg9b/mBaFG491ImIrJRBfKb2PPAqMxsjPfz4RmCfme1090PZOm8DHmpTey9wlZldBrxAeoLJT1/oATY+++rnptJBYIXf2Rf99xMpEt0kdJm5+zfM7K+A+4A68G3gduAjZnYd6cTlWeCXAMxsF+mp+7e4e93M3g38Dekp/R9z94dX+ncQEZHVaSBnP7r7+4H3tyz+2Q7rHgRuaXr8BeCc69dERETUUURERApDoSYiIoWhUBMRkcIYVEcRERFZARey9+MwnEWpmVob7k4t9vPoZ6hz3kVEBkGh1qKeOMdnYn7o6q1cvm2M0VL+t6gUGo++eJbTszFxt2aSLQyYqSXEiePe28VxcZJ2Fum1rqHPMhGRVUmhlnF3zszFHJ+JiR12bRzhz97xCt7zhpcwWgq6dggJDKLAuO7SbbzxZZfywOEqjx2tUs8RUgZsGAnYvb5ELYFqnNbkCalSAGOldFyNYOsl3BptutwVbiJSDPpMDZirJ5yeS85pIhmY8bZXXMQPXrWFD/7t03ztqRPn9ICMAuOijWO8+nt2MjFSml9+ZCrm+MwMV24usW08ImzpAWlAJTS2jUeLAjP2tNFxKUjvINCu9VUAjJTsnFvQJJ51+8gSKm/bLG/5QR1DRGRYrelQixPn9FzMUu0dN42V+O3/4Wru23+Kf/f5Jzg1Uyd2JwwCXnf1Ti7euq5tXT2BR4/WeOF0zDXby1RCy5oVw9axiPFS536NtcSpJ1AJG30W0/XK4UKvx3bc02wKLJ25pavlD7emTFS4iRSA2mStITO1ZMlAa3b9xRv4q3dez4f+7nmePj7HKy7dShQufQT3TDXhmwdmecVFFS7ZGLF5NMp1o08HZmOnEhqVACo9NDxOvL9O+o1Zm/JMRIbRmg61fpTCgJuvvYhvHpjJfVdoSMNiuuZsGskXaK16CbTmbSqcRGQt0YkiIiJSGAo1EREpDIWaiIgUhkJNREQKQ6EmIiKFoVATEZHCUKj1KG12nLBptPe3buNo0FefxjBYaGnVC0On9IvI2rKmr1MbKQXMxWmvxzymqgmPH5ujlsBFExFbRp39p+vM1ru/wEQ54DWXjLJpNCQBqgmUAl/yerXA0tpGG61eLowObfFF13kDUSEoIsNsTYdaFBibR0NmaglTNe+4448T57mTNV48WyeZbyFllCPjsk0lTs8mHGp6riEwuHZHhZduq2QhsxAZtQQCnCho36NxNDLGysH8thoaM7ZOs7DA0q/WusYv1y3c+ulAIiKymqzpUIN0xz9WDhkpOafnEqot07bj0zGPH5sjcc4JLUibHm8cDVlXCTh4ps7pubTv1o6JkNdcPEYlsnOaGTc0Zm2h+XzoRQGsq4QE1r0hcbtwi4KF3+nc3zPt6WicG2wKM5HiynOT0CL1hlzzodYQmLFxJKQapx37Z+vO40fnOD2XtA2zVmFg7F4fsSN2dm+I2DFRIuoQZq3i7NYvG0cDRnpsh+Wkhxrbzs5azD/V5vdRoIlIEehEkRblMGDLaMiJ6TonZ/MFWkNgxs71JXauyx9oDZXIeg40SP+AjVld3lpr+ryt+WcRkWGnUGvDzHJ1329bS58nW1jvZzeeL4WZiBSNQk1ERApDoSYiIoWhE0VERApsrd35eiAzNTP7VTN72MweMrNPmtmImf2emT1qZt8xszvMbGOH2mfN7EEzu9/M9q302EVEZPVa8VAzs93Ae4C97n4tEAK3AvcA17r7y4HHgV/v8jJvcPfr3H3vsg9YRESGxqA+U4uAUTOLgDHgoLvf7e717PmvA3sGNDYRERlSKx5q7v4C8EHgeeAQcMrd725Z7eeBL3Z6CeBuM/uWmd3WaTtmdpuZ7TOzfZOTk72OkbiXC9QuBFffRRG5MM5n/zfsVvxEETPbBLwVuAw4Cfylmf2Mu/8/2fO/CdSBP+/wEq9194Nmth24x8wedfevtK7k7rcDtwPs3bs3d0LVE+fsXMKm0ZCJsjFd89wXYAcGU9WYOIkIA+/pQupqnG4noLe6hOz6Ntd1ZyKSat7/Xf7Sl3u7NllFPXlkEIcf3wQ84+6T7l4D/hp4DYCZvQP4UeB/9g73Z3H3g9n3I8AdwA0XYlDuztm5mFOzCbHDSBRw/c5RrtxcTvsyLlFvwJbRgD3rS1Rjpxp77lvMTJSMrWMhwPytafLUGhBZ+pOTttrq8a42IiKFMohT+p8HXmVmY8AM8EZgn5ndDPwa8E/cfbpdoZmNA4G7n8l+/mHg35/PYNydapzeVuacRr9m7FxXYutYxJPH5zg6HZ8zazNgrGTsmIgWtcaKE5hJnFJIx078pQA2jITntNRKGrMu92z2tfh5g3O6/kNTR5L5OwnkeANERApkxUPN3b9hZn8F3Ed6mPHbpNPkh4EK6SFFgK+7+y+b2S7gI+5+C7ADuCN7PgI+4e539TuWOHHOVhPqSff1SqHx0m0jnJqNefToXDYLSw83XjQRMV7uPOGtxU49gUqUtdAyw4ANIwGVsHO/Rvc0m9JXXjgk2dzrsZNG935XuInIGjOQi6/d/f3A+1sWX9lh3YPALdnPTwOvuFDjmK0vHWjNNoyE/MDuUZ4+McdMzdk8Gi55o09Iw2W25oyXA0YjmKjkq4N01hZY59lZx21m35VnIrKWqKNIjwIzLpoocWauhzScr+0t0Jr1EmgiImuVQk1EpMDUJktERGRIKdRERKQwFGoiIlIYCjURESkMhZqIiBSGQq1HjhMFaReRXo2GRtjHWfmN69RERKS7NX1K/0gUUIvTXo95eHZJcyUMKIfOWBlOzcTUcnQk2TkRUYlsPpxi55y2XK0MKIdGcxetvK0dFYIishat6VALA2PDSMBc3ZmqdY4Lb40SA8OIDDaPhczWndOzbXpHAlvGQjaNhvMtsua3nb1qp0CNAihlabboomtf9K2txtq6VltE1po1HWqQBsZIyShHzlQ1oRovPHdOmHWqj6AyEXJ6NmG2ntaMldJmyIHRtoOImYE7kaWtsBqTvcDS2VlrCC7UpW23jHODTWEmImvdmg+1hsCMdZWQWpw2OY57uIdLo0nx+pGAiQRGImO0FCzZDmuhSbGnjYoDy9UOa/7pNkNUoInIWqYTRVqUQmPjSDB/6K8XgRljpYCxHIHWzMwIgt77O5othFjzzyIiDcenqrS7SWhRKdTaMDNK/ZymeH5b7b9SYSYiAijURESkQBRqIiJSGAo1EREpDIWaiIgUhkJNRKTAdJNQERGRIaVQa8PdSXq4+FpERFYHhVqLxJ16kvZd7OdStXriJKTB2AvPGhwrS0VE+qc2WRl3J04WOk8FZoyXAmqxM5OzjX8pgCgwkiygwuzVlmx7ReMCaksrss3pomoRkd6s+VBzd9zbd8s3M8qRUQqdmXrS8RYzgUEltEXh5UDd0+cC9/nQalfbGnqerekKNxGRnqzpUGudnXViZoyVQuqJM1NL5jvqN+53FnbpE9nowB+SzsPmmxgv0eexMSaFm4icj+NT1UEPYUWt6VDLE2jNosCYKAfM1tNgKwWWuwFx7FnDYpYOtGbN4SYiIt0N5EQRM/tVM3vYzB4ys0+a2YiZbTaze8zsiez7pg61N5vZY2b2pJm9bwBjpxwFlMOgp476Db0EmoiI9GbFQ83MdgPvAfa6+7WkR+ZuBd4HfMndrwK+lD1urQ2BPwTeAlwD/JSZXbNSYxcRkdVtUKf0R8ComUXAGHAQeCvw8ez5jwM/3qbuBuBJd3/a3avAp7I6ERGRlQ81d38B+CDwPHAIOOXudwM73P1Qts4hYHub8t3A/qbHB7JlIiIiAzn8uIl0dnUZsAsYN7OfyVveZlnbcz3M7DYz22dm+yYnJ/sbrIjIEGre/8XTpwY9nBU1iMOPbwKecfdJd68Bfw28BjhsZjsBsu9H2tQeAC5ueryH9NDlOdz9dnff6+57t23bdkF/ARGR1Wwt7/8GEWrPA68yszFLTwN8I/AIcCfwjmyddwCfbVN7L3CVmV1mZmXSE0zuXIExi4jIEFjx69Tc/Rtm9lfAfUAd+DZwOzABfNrMfoE0+P4ZgJntAj7i7re4e93M3g38DelZkx9z94dX+ncQEZHVaSAXX7v7+4H3tyyeI521ta57ELil6fEXgC9ciHGEQe8XYMPC9LZD16yOEldXEBGR5bSmO4qYGWHgaSurnMkWGARZW6zYodpjs2Mzm+/In3ucKAxFRPJY06EGWbBlTYe7zdqMdGbX3A0ksrT1VTX2tg2RoX2zYzMgR7ApzEREerPmQ63BzIjC9H5qcctxxTBIb0XTqa4SGYk7c3Vf1KuxW7Njs4Vmxa3hpjATEemPQq1FYIZlhyTTx/l6NQZmjETpTUKd/M2OW2dtCjQRkf4p1NpoHJLsp67UR2Fj1iYiIudnUL0fRURELjiFmoiIFIZCTURECkOhJiIihWHuvfbTGD5mNgk8l2PVrcDRZR7OctL4B2eYxw4a/yD1M/aj7n5znhXN7K686xbBmgi1vMxsn7vvHfQ4+qXxD84wjx00/kEa5rGvRjr8KCIihaFQExGRwlCoLXb7oAdwnjT+wRnmsYPGP0jDPPZVR5+piYhIYWimJiIihaFQExGRwlCoZczsZjN7zMyeNLP3DXo8SzGzZ83sQTO738z2Zcs2m9k9ZvZE9n3ToMfZYGYfM7MjZvZQ07KO4zWzX8/+Fo+Z2T8dzKgXdBj/vzWzF7K/wf1mdkvTc6tm/GZ2sZl92cweMbOHzey92fKheP+7jH/Vv/9mNmJm3zSzB7Kx/7ts+VC890PJ3df8FxACTwGXA2XgAeCaQY9riTE/C2xtWfa7wPuyn98H/M6gx9k0tpuA64GHlhovcE32N6gAl2V/m3AVjv/fAv+6zbqravzATuD67Od1wOPZGIfi/e8y/lX//pPegGMi+7kEfAN41bC898P4pZla6gbgSXd/2t2rwKeAtw54TP14K/Dx7OePAz8+wLEs4u5fAY63LO403rcCn3L3OXd/BniS9G80MB3G38mqGr+7H3L3+7KfzwCPALsZkve/y/g7WTXj99TZ7GEp+3KG5L0fRgq11G5gf9PjA3T/P81q4MDdZvYtM7stW7bD3Q9BuiMAtg9sdPl0Gu8w/T3ebWbfyQ5PNg4hrdrxm9lLgFeSzhiG7v1vGT8MwftvZqGZ3Q8cAe5x96F874eFQi3V7h6dq/1ah9e6+/XAW4B3mdlNgx7QBTQsf48PA1cA1wGHgA9ly1fl+M1sAvgM8Cvufrrbqm2WrcbxD8X77+6xu18H7AFuMLNru6y+qsY+jBRqqQPAxU2P9wAHBzSWXNz9fJnxNwAAAv5JREFUYPb9CHAH6SGKw2a2EyD7fmRwI8yl03iH4u/h7oezHVYC/AkLh4lW3fjNrEQaCH/u7n+dLR6a97/d+Ifp/Qdw95PA3wM3M0Tv/bBRqKXuBa4ys8vMrAzcCtw54DF1ZGbjZrau8TPww8BDpGN+R7baO4DPDmaEuXUa753ArWZWMbPLgKuAbw5gfF01dkqZt5H+DWCVjd/MDPgo8Ii7/8emp4bi/e80/mF4/81sm5ltzH4eBd4EPMqQvPdDadBnqqyWL+AW0rOqngJ+c9DjWWKsl5OeIfUA8HBjvMAW4EvAE9n3zYMea9OYP0l6iKhG+q/RX+g2XuA3s7/FY8BbVun4/wx4EPgO6c5o52ocP/A60kNY3wHuz75uGZb3v8v4V/37D7wc+HY2xoeAf5MtH4r3fhi/1CZL5P9v7w5ZrAijMI7/H9wggmWjQbboNk03CEY/giIWTSIK4jcwWI2bFIOCQcFoWayroAuCIrrdYHZBFFGOYd4bXC73Bkeuvvv/pbnDO5cz6eGdGc6R1A0fP0qSumGoSZK6YahJkrphqEmSumGoSZK6YahJI0hyK8mZZdch7Xd+0i/9oSQHqurnsuuQ5E5NmivJWpKdJA9a49wnSQ5lmGd3M8kWcC7J/SRn2zWTJC/aDK1XSQ63pra3k2y3/7my5FuTumSoSYutA3er6gSwC1xr579V1emqejRd2NqsPQZuVNVJhrZIXxk6kHyuqgkwAS63NkiSRmSoSYt9rKrn7fghQ9smGMJrr3XgU1VtA1TVblX9YOjPebGNIHnJ0Cbp2N8tW9p/VpZdgPQf2Pviefr7y4y1mbF+ev56VW2OWZik37lTkxY7muRUO74AbM1ZuwMcSTIBaO/TVoBN4GoboUKS423CgqQRGWrSYh+AS0neAqsMwylnqqrvwHlgI8kb4BlwELgHvAdeJ3kH3MEnJdLo/KRfmiPJGvC0quZNK5b0j3CnJknqhjs1SVI33KlJkrphqEmSumGoSZK6YahJkrphqEmSuvELapGxVuvKbqUAAAAASUVORK5CYII=
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Data-Analysis">Data Analysis<a class="anchor-link" href="#Data-Analysis">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Shows simple prediction methods cant acurately predict the score of a wine based off of the parameters used above.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Note:">Note:<a class="anchor-link" href="#Note:">&#182;</a></h2><p>idk which one we want to include</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[13]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">X</span> <span class="o">=</span> <span class="n">wine_df</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;points&#39;</span><span class="p">],</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span><span class="o">.</span><span class="n">to_numpy</span><span class="p">(</span><span class="s1">&#39;int64&#39;</span><span class="p">)</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">wine_df</span><span class="p">[</span><span class="s1">&#39;points&#39;</span><span class="p">]</span>
<span class="n">X</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[13]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([[                   0, -9223372036854775808,                    0,
        ...,                    0,                    0,
                           0],
       [                   1,                   15,                    1,
        ...,                    1,                    1,
                           1],
       [                   2,                   14,                    2,
        ...,                    2,                    2,
                           2],
       ...,
       [                   4,                   30,                    5,
        ...,                    1,                    7,
                       10215],
       [                   4,                   32,                    5,
        ...,                    1,                    2,
                        5348],
       [                   4,                   21,                    5,
        ...,                    1,                    7,
                        2777]])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[14]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">X_train</span><span class="p">,</span> <span class="n">X_test</span><span class="p">,</span> <span class="n">y_train</span><span class="p">,</span> <span class="n">y_test</span> <span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">X</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="n">random_state</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="linear-regression">linear regression<a class="anchor-link" href="#linear-regression">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[15]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">model</span> <span class="o">=</span> <span class="n">linear_model</span><span class="o">.</span><span class="n">LinearRegression</span><span class="p">()</span>
<span class="n">model</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span> <span class="n">y_train</span><span class="p">)</span>
<span class="n">model</span><span class="o">.</span><span class="n">coef_</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[15]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([-4.65322364e-09, -5.12190003e-20, -8.97987981e-08, -5.55497062e-07,
        2.36155973e-10, -1.03702590e-07, -8.99944558e-05])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[16]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">model</span><span class="o">.</span><span class="n">score</span><span class="p">(</span><span class="n">X_test</span><span class="p">,</span><span class="n">y_test</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[16]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>0.015686482196156426</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="linear-discriminant-analysis">linear discriminant analysis<a class="anchor-link" href="#linear-discriminant-analysis">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[17]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">lda_model</span> <span class="o">=</span> <span class="n">LinearDiscriminantAnalysis</span><span class="p">()</span>
<span class="n">lda_model</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span> <span class="n">y_train</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[17]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>LinearDiscriminantAnalysis()</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[18]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">lda_model</span><span class="o">.</span><span class="n">score</span><span class="p">(</span><span class="n">X_test</span><span class="p">,</span><span class="n">y_test</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[18]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>0.13904533284091958</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="classification-tree">classification tree<a class="anchor-link" href="#classification-tree">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[19]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">dt_model</span> <span class="o">=</span> <span class="n">tree</span><span class="o">.</span><span class="n">DecisionTreeClassifier</span><span class="p">()</span>
<span class="n">dt_model</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span> <span class="n">y_train</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[19]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>DecisionTreeClassifier()</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[20]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">dt_model</span><span class="o">.</span><span class="n">score</span><span class="p">(</span><span class="n">X_test</span><span class="p">,</span><span class="n">y_test</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[20]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>0.24356015141722834</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="kNN">kNN<a class="anchor-link" href="#kNN">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[21]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">n</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">floor</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">sqrt</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">wine_df</span><span class="p">))))</span>
<span class="n">neigh</span> <span class="o">=</span> <span class="n">KNeighborsClassifier</span><span class="p">(</span><span class="n">n_neighbors</span><span class="o">=</span><span class="n">n</span><span class="p">)</span>
<span class="n">neigh</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_test</span><span class="p">,</span> <span class="n">y_test</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[21]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>KNeighborsClassifier(n_neighbors=360)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[22]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">neigh</span><span class="o">.</span><span class="n">score</span><span class="p">(</span><span class="n">X_test</span><span class="p">,</span><span class="n">y_test</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[22]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>0.1538177453605392</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Random-Forrest">Random Forrest<a class="anchor-link" href="#Random-Forrest">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># takes a LONG time to run</span>

<span class="n">rf_model</span> <span class="o">=</span> <span class="n">RandomForestClassifier</span><span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">100</span><span class="p">)</span>
<span class="n">rf_model</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span> <span class="n">y_train</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">rf_model</span><span class="o">.</span><span class="n">score</span><span class="p">(</span><span class="n">X_test</span><span class="p">,</span><span class="n">y_test</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><strong>Note:</strong> In all of these analysis the the text description of the review isnt used. If its included can we do better?</p>

</div>
</div>
</div>
    </div>
  </div>
</body>

 


</html>
