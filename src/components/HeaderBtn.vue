<template>
  <button class="btn"> Sign in</button>
  <button class="btn -s"> Sign Up</button>
  <MenuHamburguer/>
</template>

<script>
import MenuHamburguer from "./MenuHamburguer"
export default {
  name:'HeaderBtn',
  components:{
    MenuHamburguer
  }
}
</script>

<style lang="scss">
.btn {
 position: relative;
 font-size: 17px;
 text-transform: uppercase;
 text-decoration: none;
 padding: .5em 2.5em;
 display: inline-block;
 border-radius: 6em;
 transition: all .2s;
 border: none;
 font-family: inherit;
 font-weight: 500;
 color: #8794BA;
 background-color: transparent;
 cursor: pointer;
 @media screen and (max-width:882px) {
    font-size: 12px;
    padding: .5em .5em;
  }
}
.-s{
  display: none;
  border: 1px solid #465B95;
  @media screen and (min-width:882px) {
    display: block;
  }
}
.btn:hover {
 transform: translateY(-3px);
 box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
 background-color: #465B95;
}

.btn:active {
 transform: translateY(-1px);
 box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}

.btn::after {
 content: "";
 display: inline-block;
 height: 100%;
 width: 100%;
 border-radius: 100px;
 position: absolute;
 top: 0;
 left: 0;
 z-index: -1;
 transition: all .4s;
}

.btn::after {
 background-color: #465B95;
}

.btn:hover::after {
 transform: scaleX(1.4) scaleY(1.6);
 opacity: 0;
}
  
</style>