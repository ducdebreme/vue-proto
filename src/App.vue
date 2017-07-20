<template>
  <div id="app">
    <autocomplete url="http://localhost:10000/ubs_shared/autocomplete/user/" :custom-params="{ token: 'dev' }" anchor="title" label="writer" :on-select="getData">
    </autocomplete>
  
    <h2>Essential Links</h2>
    <ul>
      <li>
        <a href="https://vuejs.org" target="_blank">Core Docs</a>
      </li>
      <li>
        <a href="https://forum.vuejs.org" target="_blank">Forum</a>
      </li>
      <li>
        <a href="https://gitter.im/vuejs/vue" target="_blank">Gitter Chat</a>
      </li>
      <li>
        <a href="https://twitter.com/vuejs" target="_blank">Twitter</a>
      </li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li>
        <a href="http://router.vuejs.org/" target="_blank">vue-router</a>
      </li>
      <li>
        <a href="http://vuex.vuejs.org/" target="_blank">vuex</a>
      </li>
      <li>
        <a href="http://vue-loader.vuejs.org/" target="_blank">vue-loader</a>
      </li>
      <li>
        <a href="https://github.com/vuejs/awesome-vue" target="_blank">awesome-vue</a>
      </li>
    </ul>
    <div class="block">
      <a class="button">Button</a>
      <a class="button is-white">White</a>
      <a class="button is-light">Light</a>
      <a class="button is-dark">Dark</a>
      <a class="button is-black">Black</a>
      <a class="button is-link">Link</a>
    </div>
    <div class="block">
      <a class="button is-primary">Primary</a>
      <a class="button is-info">Info</a>
      <a class="button is-success">Success</a>
      <a class="button is-warning">Warning</a>
      <a class="button is-danger">Danger</a>
    </div>
  </div>
</template>

<script>
import Autocomplete from './components/vue-autocomplete.vue';

export default {
  name: 'app',
  components: {
    Autocomplete
  },
  methods: {
    getData(data) {
      console.log(data);
    }
  },
  data() {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style lang="sass">
// customizing bulma, @see http://bulma.io/documentation/overview/customize/

// 1. Import the initial variables
@import "~bulma/sass/utilities/initial-variables"

// 2. Set your own initial variables
// Update blue
// $blue: #72d0eb
// Add pink and its invert
// $pink: #ffb3b3
// $pink-invert: #fff
// Add a serif family
// $family-serif: "Merriweather", "Georgia", serif

// 3. Set the derived variables
// Use the new pink as the primary color
// $primary: $pink
// $primary-invert: $pink-invert
// Use the existing orange as the danger color
// $danger: $orange
// Use the new serif family
// $family-primary: $family-serif

// 4. Import the rest of Bulma
@import "~bulma";

// @import '~bulma/sass/utilities/_all';
// @import '~bulma/sass/elements/button.sass';
</style>
 