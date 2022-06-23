<script setup></script>

<template>
  <body>
    <header>
      <div class="circle"></div>
      <div class="testo"></div>
      
    </header>

    <main>
      <div class="corpao">
        
        <nav></nav>
      </div>
    </main>
  </body>
</template>

<style>
@import "@/assets/base.css";

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;

  font-weight: normal;
}

body {
  background-color: #CCB8D4;
}
header{

width: 100px;
height: 100px;
border-radius: 50%;
background-color: #A882B7;
margin: 50px;


}
.corpao{
  background-color:#F9E5F0 ;

}

.testo{
  padding: 10%;
  align-content: center;
  justify-content: center;
}
</style>
