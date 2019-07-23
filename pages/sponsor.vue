<template>
  <div>
    <nav class="navbar is-fixed-bottom" role="navigation" aria-label="main navigation">
      <div class="navbar-menu is-active"
           v-bind:class="{ 'is-down': burger, 'navmenusmall': ($mq !== 'threecards' && $mq !== 'fourcards' && $mq !== 'desktop') }">
          <div class="menuitemcontainer"><a href="https://info.ogd.nl/" target="_blank"><img src="~assets/sponsors/ogd.jpg" class="small-image"/></a></div>
          <div class="menuitemcontainer"><a href="https://www.stud.nl/" target="_blank"><img src="~assets/sponsors/stud.svg" class="small-image"/></a></div>
          <div class="menuitemcontainer"><a href="https://www.lunatech.com/" target="_blank"><img src="~assets/sponsors/lunatech.png" class="small-image"/></a></div>
          <div class="menuitemcontainer"><a href="https://www.makro.nl/" target="_blank"><img src="~assets/sponsors/makro.png" class="small-image"/></a></div>
          <div class="menuitemcontainer"><a href="https://www.printerpro.nl/home/" target="_blank"><img src="~assets/sponsors/printerpro.jpg" class="small-image"/></a></div>
          <div class="menuitemcontainer"><a href="https://www.tradecloud1.com/nl/" target="_blank"><img src="~assets/sponsors/tradecloud.png" class="small-image"/></a></div>
      </div>
    </nav>
  </div>
</template>

<style scoped>

  .small-image{
    max-height: 50px;
  }

  .navbar-menu{
    background-color: white;
    text-align: center;
    width: 100%;
    padding: 0;
    position: fixed;
    border-top: 5px solid #f5eb22;
    transition: 0.2s ease all;
  }

  .navbar-menu a {
    width: 100%;
    height: 100%;
    display: block;
  }

  .menuitemcontainer{
    line-height: 2.5;
    transition: 0.2s ease all;
    border-radius: 10px;
    text-align: center;
    padding: 0px 4%;
  }

  .navbar-brand img{
    position: relative;
    bottom: 7px;
    height: 50px;
  }
</style>
