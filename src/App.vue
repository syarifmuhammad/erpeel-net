<script setup>
import Navbar from './components/Navbar.vue'
import Jumbotron from './components/Jumbotron.vue'
import Fitur from './components/Fitur.vue'
import Paket from './components/Paket.vue'
import FooterCustom from './components/Footer.vue'
</script>

<template>
  <navbar></navbar>
  <jumbotron></jumbotron>
  <fitur></fitur>
  <paket></paket>
  <footer-custom></footer-custom>
</template>

<style>
@font-face {
  font-family: "TelkomselBatikSans-Bold";
  src: local("TelkomselBatikSans-Bold"),
    url(./assets/fonts/TelkomselBatikSans-Bold.woff2) format("truetype");
}
</style>
