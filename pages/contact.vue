<template>
  <div id="contact">
    <div class="content">

      <h2 v-if="$cookie.get('language') == 'dutch'">Waar kan je ons vinden?</h2>
      <h2 v-if="$cookie.get('language') == 'english'">Where can you find us?</h2>

      
      <p>
        De Bolk (D.S.V. "Nieuwe Delft")<br/>
        Buitenwatersloot 1-3<br/>
        2613 TA Delft
      </p>

      <p>
      Telefoon/Phone: 015 212 6012<br/>
      E-mail: <a href="mailto:owee@nieuwedelft.nl">owee@nieuwedelft.nl</a><br/>
      Website: <a href="http://www.debolk.nl">www.debolk.nl</a>
      </p>
    </div>

  </div>
</template>

<style>

#contact p{
  color: white;
}

#contact a{
  color: white;
  text-decoration: underline;
}

#contact a:hover{
  color: #f5eb22;
}

#contact{
  background-color: #0d8141;
  padding: 100px 0px;
  position: relative;
  text-align: center;
}

.maintriangles{
  height: 50px;
  width: 100%;
  position: absolute;
  bottom: 0px;
  background-image: url('~/assets/triangle-yellow.svg');
  background-size: contain;
}
</style>
