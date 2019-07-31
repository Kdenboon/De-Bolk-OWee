<template>
  <div id="header">
    <div id="imageheader">
      <img v-bind:class="{ 'mobileheaderlogo': $mq === 'mobile' }"
        class="largelogo"
        src="~/assets/owee-logo-geel.svg">
      <br/>
      <img v-bind:class="{ 'mobileheadertext': $mq === 'mobile' }"
        class="largetext"
        src="~/assets/Tekst svg versie 2.svg">
      <div class="triangles"></div>
    </div>
  </div>
</template>

<style>
  #imageheader{
    background-image: url('~/assets/fotos/DSC_0316.jpg');
    background-size: cover;
    width: 100%;
    height: 100vh;
    border: 10px solid #0d8141;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 0 20px;
  }

  .triangles{
    height: 50px;
    width: 100%;
    position: absolute;
    top: calc(100vh - 60px);
    background-image: url('~/assets/triangle-green.svg');
    background-size: contain;
  }

  .largelogo{
    height:50vw;
    background-repeat: no-repeat;
    margin-right: 20px;
    max-height: 50vh;
  }

  .largetext{
    height:75vw;
    background-repeat: no-repeat;
    max-height: 75vh;
  }

  #imageheader .mobileheadertext{
    height: 30vw !important;
    background-repeat: no-repeat;
    max-height: 30vh;
  }

  #imageheader .mobileheaderlogo{
    height: 30vw !important;
    background-repeat: no-repeat;
    max-height: 30vh;
  }

  #imageheader h1{
    font-size: 8rem !important;
    color: #f5eb22 !important;
    text-shadow: -4px 0 #0d8141,
                -4px -4px #0d8141,
                4px 4px #0d8141,
                -4px 4px #0d8141,
                4px -4px #0d8141,
                0 4px #0d8141,
                4px 0 #0d8141,
                0 -4px #0d8141;
  }
</style>
