<template>
  <div>
    <ul class="timeline">
      <li data-year="2017" data-text="Invented PDC Mining Technology"></li>
      <li
        data-year="2019"
        data-text="Technical Contribution to the IPFS project"
      ></li>
      <li data-year="2019" data-text="Proposed the application concept"></li>
      <li
        data-year="2020"
        data-text="Obtained Investment from Y.C and IDC fund"
      ></li>
    </ul>

    <div class="flex">
      <form  class="flex-item">
        <button id="greater" style="font-size: 20px"><b>&gt;</b></button>
      </form>

      <form  class="flex-item">
        <button id="greater" style="font-size: 20px;"><b>&#60;</b></button>
      </form>
    </div>
  
    <div id="blur" style="line-height:0%;" >Progress</div>
    <p style="text-align:center;position:sticky;color:white;font-size:31px;"><b>Project Development Progress</b></p>
   
    
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style>

#blur {
        font-size: 246px;
     text-align: center;
     color:#848884;
       -webkit-filter: blur(1px);
       padding-top:3%;

      }
.flex {
  display: flex;
  justify-content: center;
  padding-top:5%;
}

.flex-item + .flex-item {
  margin-left: 10px;
}

body {
  width: 100vw;
  height: 100vh;
  background-color: #00008b;
}
#greater {
  display: block;
  height: 50px;
  width: 50px;
  border-radius: 50%;
  border: 1px solid #add8e6;
  background-color: transparent;
  color:white;
}
.timeline {
  width: 800px;
  height: 20px;
  list-style: none;
  text-align: justify;
  margin: 80px auto;
  background: linear-gradient(
    to bottom,
    rgba(255, 255, 255, 0) 0%,
    rgba(255, 255, 255, 0) 45%,
    black 51%,
    rgba(255, 255, 255, 0) 57%,
    rgba(255, 255, 255, 0) 100%
  );
}
.timeline:after {
  display: inline-block;
  content: "";
  width: 100%;
}
.timeline li {
  display: inline-block;
  width: 20px;
  height: 20px;

  background: #0000ff;
  text-align: center;
  line-height: 1.2;
  position: relative;
  border-radius: 50%;
  box-shadow: 0px 0px 15px 15px #add8e6;
}

.timeline li:before {
  display: inline-block;
  content: attr(data-year);
  font-size: 26px;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  padding-top: 30px;
  color: white;
}
.timeline li:after {
  display: inline-block;
  content: attr(data-text);
  font-size: 16px;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  padding-top: 60px;
  color: white;
}
</style>
