<div class="hr">
  <span>hello</span>
</div>

.hr {
  width: 100%;
  color: #d9444a;
  text-align: center;
  border-top: 2px solid gray;
  line-height: 0;
}

span {
  background: #fff;
  padding: 0 10px;
}





<h1>
  <span> hello</span>
</h1>

h1{
  text-align: center;
}

h1::before {
  content: "";
  position: absolute;
  top: 50%;
  left: 0;
  width: 100%;
  border-top: 4px solid #EAEEEF;
}

span {
  position: relative;
  display: inline-block;
  padding: 0 1em;
  background: #fff;
}
