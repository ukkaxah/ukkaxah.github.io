

<div class="container">
  <div class="wrap">
    <div class="circle horizontal c1">
      <div class="wrap-electron">
        <div class="circle electron"></div>
      </div>
    </div>
    <div class="circle vertical c1">
      <div class="wrap-electron">
        <div class="circle electron"></div>
      </div>
    </div>
  </div>
  <div class="wrap r">
    <div class="circle horizontal c2">
      <div class="wrap-electron">
        <div class="circle electron"></div>
      </div>
    </div>
    <div class="circle vertical c2">
      <div class="wrap-electron">
        <div class="circle electron"></div>
      </div>
    </div>
    <div class="circle center"></div>
  </div>
</div>

@background: #222;
@center-background: #999;

@border-color: #666;
@border-size: 3px;

@border-color-c2: #555;
@border-size-c2: 2px;

@size: 250px;
@size-c2: 140px;
@size-center: 30px;

@t-wrap-1: 15s;
@t-wrap-2: 8s;

@t-ho-c1: 8s;
@t-ve-c1: 6s;

@t-ho-c2: 4s;
@t-ve-c2: 3s;

@t-el-c1-a: 3s;
@t-el-c1-b: 1s;
@t-el-c2-a: 2s;
@t-el-c2-b: 30s;

body{
    background: @background;
}

.container{
    position:relative;
    margin:auto;
    width: @size;
}

.wrap, .circle{
    -webkit-transition: -webkit-transform 500ms linear;
    -webkit-transform-style: preserve-3d;
    -moz-transition: -moz-transform 500ms linear;
    -moz-transform-style: preserve-3d;
    width:@size;
    height:@size;
    margin:auto;
    margin-top:50px;
    position:absolute;
}

.circle{
    position:absolute;
    border:@border-size solid @border-color;
    border-radius: @size;
    margin:auto;
}

.circle.c2,
.circle.center{
    border:@border-size-c2 solid @border-color-c2;
    width: @size-c2;
    height: @size-c2;
    top: round( (@size - @size-c2) / 2 );
    left: round( (@size - @size-c2) / 2 );
}
.circle.center{
    background: @center-background;
    width: @size-center;
    height: @size-center;
    top: round( (@size - @size-center) / 2 );
    left: round( (@size - @size-center) / 2 );
    box-shadow: 0 0 5px #fff;
}

.wrap-electron{
  border:0px solid  #fff;
  position:absolute;
  width:100%;
  height:100%;
  -webkit-animation: electron @t-el-c1-a linear infinite;
  -moz-animation: electron @t-el-c1-a linear infinite;
}

.electron{
  width:12px;
  height:12px;
  background: @border-color;
  left:50%;
  margin-left:-8px;
  border:none;
  top:-7px;
  -webkit-transform-origin:50% 50%;
}

.c2 .wrap-electron{
  -webkit-animation: electron @t-el-c2-a linear infinite;
  -moz-animation: electron @t-el-c2-a linear infinite;
}

.c2 .electron{
  top:-6px;
}




.wrap{
    border:0px solid @border-color;
    -webkit-animation: lateral @t-wrap-1 ease-in-out infinite;
    -moz-animation: lateral @t-wrap-1 ease-in-out infinite;
}

.wrap.r{
    -webkit-animation: lateralRevert @t-wrap-2 linear infinite;
    -moz-animation: lateralRevert @t-wrap-2 linear infinite;
}


.vertical{
    -webkit-animation: vertical @t-ho-c1 linear infinite;
    -moz-animation: vertical @t-ho-c1 linear infinite;
}
.horizontal{
    -webkit-animation: horizontalRevert @t-ve-c1 linear infinite;
    -moz-animation: horizontalRevert @t-ve-c1 linear infinite;
}

.vertical.c2{
    -webkit-animation: vertical @t-ho-c2 linear infinite;
    -moz-animation: vertical @t-ho-c2 linear infinite;
}


.horizontal.c2{
    -webkit-animation: horizontalRevert @t-ve-c2 linear infinite;
    -moz-animation: horizontalRevert @t-ve-c2 linear infinite;
}

@-webkit-keyframes electron {
  from {
      -webkit-transform: rotateZ(0deg);
  }
  to {
      -webkit-transform: rotateZ(360deg);
  }
}



@-webkit-keyframes horizontal {
  from {
      -webkit-transform: rotateY(0deg);
  }
  to {
      -webkit-transform: rotateY(360deg);
  }
}

@-webkit-keyframes horizontalRevert {
  from {
      -webkit-transform: rotateY(360deg);
  }
  to {
      -webkit-transform: rotateY(0deg);
  }
}

@-webkit-keyframes vertical {
  from {
      -webkit-transform: rotateX(0deg);
  }
  to {
      -webkit-transform: rotateX(360deg);
  }
}

@-webkit-keyframes verticalRevert {
  from {
      -webkit-transform: rotateX(360deg);
  }
  to {
      -webkit-transform: rotateX(0deg);
  }
}


@-webkit-keyframes lateral {
  from {
      -webkit-transform: rotateZ(0deg);
  }
  to {
      -webkit-transform: rotateZ(360deg);
  }
}

@-webkit-keyframes lateralRevert {
  from {
      -webkit-transform: rotateZ(360deg);
  }
  to {
      -webkit-transform: rotateZ(0deg);
  }
}

@-moz-keyframes electron {
  from {
      -moz-transform: rotateZ(0deg);
  }
  to {
      -moz-transform: rotateZ(360deg);
  }
}


@-moz-keyframes horizontal {
  from {
      -moz-transform: rotateY(0deg);
  }
  to {
      -moz-transform: rotateY(360deg);
  }
}

@-moz-keyframes horizontalRevert {
  from {
      -moz-transform: rotateY(360deg);
  }
  to {
      -moz-transform: rotateY(0deg);
  }
}

@-moz-keyframes vertical {
  from {
      -moz-transform: rotateX(0deg);
  }
  to {
      -moz-transform: rotateX(360deg);
  }
}

@-moz-keyframes verticalRevert {
  from {
      -moz-transform: rotateX(360deg);
  }
  to {
      -moz-transform: rotateX(0deg);
  }
}


@-moz-keyframes lateral {
  from {
      -moz-transform: rotateZ(0deg);
  }
  to {
      -moz-transform: rotateZ(360deg);
  }
}

@-moz-keyframes lateralRevert {
  from {
      -moz-transform: rotateZ(360deg);
  }
  to {
      -moz-transform: rotateZ(0deg);
  }
}


## I am a Computer Science Enthusiast, researching on AI applications in healthcare. Math Geek and oocasional competitive programming bacteria.

