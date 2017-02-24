# CSS Centering

## Table

HTML
    <div class="outer">
      <div class="inner">
        <p>Hello</p>
        <div class="content"></div>
      </div>
    </div>


CSS
    .outer {
      display: table;
      width: 200px;
      height: 200px;
      background-color: gray;
    }

    .inner {
      display: table-cell;
      text-align: center;
      vertical-align: middle;
    }

    .content {
      display: inline-block;
      width: 100px;
      height: 100px;
      background-color: #9E9E9E;
    }


## Absolute

HTML
    <div class="outer">
      <div class="inner"></div>
    </div>

CSS 1
    .outer {
      position: relative;
      width: 200px;
      height: 200px;
      background-color: gray;
    }

    .inner {
      position: absolute;
      margin: auto;
      top: 0;
      bottom: 0;
      left: 0;
      right: 0;
      width: 100px;
      height: 100px;
      background-color: #9E9E9E;
    }

CSS 2
    .outer {
      position: relative;
      width: 200px;
      height: 200px;
      background-color: gray;
    }

    .inner {
      position: absolute;
      margin: -25px 0 0 -25px;
      top: 50%;
      left: 50%;
      width: 100px;
      height: 100px;
      background-color: red;
    }
## Line Height - Only for inline text

HTML
    <div class="content">Hi</div>

CSS
    .content {
      width: 100px;
      height: 100px;
      background-color: #9E9E9E;
      line-height: 100px;
      text-align: center;
    }



## Pseudo Element

HTML
    <div class="outer">
      <div class="inner"></div>
    </div>

CSS
    .outer {
      width: 200px;
      height: 200px;
      background-color: gray;
      text-align: center;
    }
    .outer::before {
      content: '';
      display: inline-block;
      height: 100%;
      vertical-align: middle;
    }
    .inner {
      display: inline-block;
      width: 100px;
      height: 100px;
      background-color: #9E9E9E;
      vertical-align: middle;
    }

## Flexbox

HTML
    <div class="outer">
      <div class="inner"></div>
    </div>

CSS
    .outer {
      width: 200px;
      height: 200px;
      background-color: gray;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .inner {
      width: 100px;
      height: 100px;
      background-color: #9E9E9E;
    }
