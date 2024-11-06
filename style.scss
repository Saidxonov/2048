/*
  Variables:
*/

$grid-max-width: 500px;
$grid-padding: 8px;
$grid-border-radius: 5px;
// white
$color-background: #f2efea;
$color-accent1: #f9d49a;
$color-accent2: #d4a8cf;
$color-list: #00d0a4, #dd7373, #7d53de, #6622cc, #00bfb2, #c06ff2, #340068,
 #3e92cc, #d8315b, #1c0b19, #1c0b19;
/**/

*,
*:before,
*:after {
 box-sizing: border-box;
}

button,
a {
 &:hover {
  cursor: pointer;
 }
}

.clearfix::after {
 content: "";
 display: block;
 clear: both;
}

html {
 min-height: 100%;
 width: 100%;
 font-size: 16px;
 font-family: "Rubik", sans-serif;
 line-height: 1.5em;
 color: #fff;
 background: #160140;
 background: linear-gradient(to top, #160140, #261535);
}

.wrapper {
 max-width: $grid-max-width;
 margin: 0 auto;
 padding: 15px;
}

h2 {
 font-style: italic;
}

/* Introduction */

.intro {
 margin-bottom: 60px;
 &_title {
  text-align: center;
  color: $color-accent1;
  font-size: 3rem;
 }
}

/**/

/* Guide instructions */

.guide {
 border-bottom: 1px solid grey;
 &:first-of-type {
  margin-top: 4rem;
  border-top: 1px solid gray;
 }
 &_arrow {
  display: inline-block;
  margin: 15px;
  font-size: 3rem;
  color: #fff;
 }
}

.controls {
 &_game,
 &_score {
  display: inline-block;
  width: 50%;
  float: left;
  @media all and (max-width: 767px) {
   width: 100%;
  }
 }
 &_game-btn {
  margin-bottom: 1rem;
  padding: 0.5em 0.75em;
  background: transparent;
  color: #f9d49a;
  outline: 2px solid #f9d49a;
  appearance: none;
  border: 5px solid transparent;
  box-shadow: inset 0 0 0px 2px #d4a8cf;
  letter-spacing: 0.1em;
  font-weight: bold;
  text-transform: lowercase;
 }
 &_score {
  display: inline-block;
  min-width: 4em;
  margin-bottom: 4rem;
  padding: 0.5em 0.75em;
  background: #0000003b;
  text-align: center;
  background: linear-gradient(90deg, #f9d49a, #d4a8cf);

  &-label,
  &-text {
   display: inline-block;
  }
  &-label {
   color: initial;
  }
  &-text {
   color: #4a3647;
   font-size: 2rem;
  }
 }
}

/**/

/*
  Gameboard:
  the container for the static grid background; and generated tiles/numbers;
*/

.gameboard {
 /* Position: relative; set for tile-container, which absolutely positions over it to match grid's dimensions; */
 position: relative;
 width: 100%;
 max-width: 500px;
 height: 100%;
 max-height: 500px;
 margin: auto;
 padding: $grid-padding;
 background: #ffffff08;
 border-radius: $grid-border-radius;
 box-shadow: 0 0 8px 0px $color-accent1;
 &::before {
  content: "";
  display: block;
  padding-bottom: 100%;
 }
}

/**/

/*
  Grid:
  Creates the static grid background and individual grid cells;
*/

.grid {
 width: 100%;
 height: 100%;
 position: absolute;
 top: 0;
 bottom: 0;
 right: 0;
 left: 0;
 margin: auto;
 &_cell {
  display: inline-block;
  height: 25%;
  width: 25%;
  padding: $grid-padding;
  float: left;
  background: rgba(238, 228, 218, 0.35);
  background-clip: content-box;
 }
}

/**/

/*
  Tile container:
  Contains the dynamically-generated tiles;
  absolutely positioned over gameboard to match grid dimensions;
*/

.tile-container {
 /* absolutely positioned over gameboard to match dimensions */
 position: absolute;
 top: 0;
 left: 0;
 right: 0;
 bottom: 0;
 margin: auto;
 border-radius: $grid-border-radius;
}

.tile {
 @extend .grid_cell; //display:table is used to vertically align number
 display: table;
 background: #eee4da;
 background-clip: content-box;
 position: absolute;
 z-index: 2;
 will-change: top, left;
 transition-property: top, left;
 transition-duration: 0.175s;
 transition-timing-function: ease-out;

 &.initialize {
  animation-name: newTile;
  animation-duration: 0.175s;
  animation-timing-function: linear;
  animation-fill-mode: forwards;
 }
 @keyframes newTile {
  0% {
   opacity: 0;
  }
  50% {
   opacity: 0;
   transform: scale(0);
  }
  75% {
   opacity: 1;
   transform: scale(0.5);
  }
  100% {
   opacity: 1;
   transform: scale(1);
  }
 }
 &_number {
  display: table-cell;
  vertical-align: middle;
  text-align: center;
  font-size: 2rem;
  font-weight: bold;
  color: white;
 }
}

@for $g from 1 through 16 {
 $h: $g + 1;
 .tile:nth-of-type(#{$g}) {
  z-index: $h;
 }
}

@for $i from 0 through 4 {
 @for $j from 0 through 4 {
  $convertX: $i * (100 / 4);
  $convertXstring: unquote("#{$convertX}" + "%");
  $convertY: $j * (100 / 4);
  $convertYstring: unquote("#{$convertY}" + "%");
  .tile[data-x="#{$convertX}"][data-y="#{$convertY}"] {
   top: $convertYstring;
   left: $convertXstring;
  }
 }
}

$i: 2;
$listCounter: 1;
// increment by * 2 until 2048
@while $i <=2048 {
 .tile_number[data-value="#{$i}"] {
  background: nth($color-list, $listCounter);
  color: #fff;
  box-shadow: 0 0 1px 1px nth($color-list, $listCounter);
 }
 $i: $i * 2;
 $listCounter: $listCounter+1;
}
