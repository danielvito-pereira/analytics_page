<template>
  <label class="burger" for="burger">
    <input type="checkbox" id="burger" @change="toggleNavigation">
    <span></span>
    <span></span>
    <span></span>
  </label>
  <div :class="['navigationA', isActive ? 'ativo' : '']">
    <ul class="ul">
      <li><a href="">Products</a></li>
      <li><a href="">Pricing</a></li>
      <li><a href="">FAQ</a></li>
      <li><a href="">Blog</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'MenuHamburguer',
  data() {
    return {
      isActive: false
    };
  },
  methods: {
    toggleNavigation() {
      this.isActive = !this.isActive;
    }
  }
};
</script>

<style lang="scss">
  .burger {
    position: relative;
    width: 24px;
    height: 23px;
    background: transparent;
    cursor: pointer;
    display: block;
    @media screen and (min-width:882px) {
      display: none;
    }
  }

  .burger input {
    display: none;
  }

  .burger span {
    display: block;
    position: absolute;
    height: 3px;
    width: 100%;
    background: #8794BA;
    border-radius: 9px;
    opacity: 1;
    left: 0;
    transform: rotate(0deg);
    transition: .25s ease-in-out;
  }

  .burger span:nth-of-type(1) {
    top: 0px;
    transform-origin: left center;
  }

  .burger span:nth-of-type(2) {
    top: 50%;
    transform: translateY(-50%);
    transform-origin: left center;
  }

  .burger span:nth-of-type(3) {
    top: 100%;
    transform-origin: left center;
    transform: translateY(-100%);
  }

  .burger input:checked ~ span:nth-of-type(1) {
    transform: rotate(50deg);
    top: 0px;
    left: 5px;
  }

  .burger input:checked ~ span:nth-of-type(2) {
    width: 0%;
    opacity: 0;
  }

  .burger input:checked ~ span:nth-of-type(3) {
    transform: rotate(-45deg);
    top: 18px;
    left: 5px;
  }
  .navigationA{
    display: none;
  }
  .navigationA.ativo{
    position: absolute;
    height: 80vh;
    width: 100%;
    display: flex;
    flex-flow: column nowrap;
    align-items: center;
    justify-content: center;
    margin-top: 5rem;
    left: 0;
    right: 0;
    top: -1rem;
    background: #172755;
    .ul{
      width: 100%;
      height: 100%;
      display: flex;
      flex-flow: column nowrap;
      align-items: center;
      justify-content:space-evenly;
      li{
        color: #8794BA;
        &:hover{}
      }
    }
  }
</style>