<template>
  <div id="app">
    <federation-page></federation-page>
    <footer></footer>
  </div>
</template>

<script>

  import CmHeader from './components/Header';
  import Footer from './components/Footer';
  import FederationPage from './components/FederationPage';
  import News from './components/News';

export default {
  name: 'app',
  components: {
      CmHeader, Footer, FederationPage, News
  }
}
</script>

<style>
#app {

}
</style>
