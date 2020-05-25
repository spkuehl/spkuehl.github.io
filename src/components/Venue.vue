<template>
  <div class="container" id="venue">
    <h3 class="header text-center">How to get there</h3>
    <p class="text-center"><small>Hotel accommodations to follow.</small></p>
    <div class="container-sm text-center map-responsive">
      <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d5360.784842772113!2d-88.04036687242393!3d42.02619641720557!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x880fafb7b8ec97b3%3A0xedd023964d77296!2sChicago%20Marriott%20Schaumburg!5e0!3m2!1sen!2sus!4v1590377290756!5m2!1sen!2sus" width="600" height="450" frameborder="0" style="border:0" allowfullscreen>></iframe>
    </div>
    <address>
      <strong>Schaumburg Marriott</strong><br>
      50 N Martingale Rd<br>
      Schaumburg, IL. 60173<br>
      P: (847) 240-0100
    </address>
  </div>
</template>

<style>
  .map-responsive{
      overflow:hidden;
      padding-bottom:56.25%;
      position:relative;
      height:0;
  }
  .map-responsive iframe{
      left:0;
      top:0;
      height:100%;
      width:100%;
      position:absolute;
  }
</style>
