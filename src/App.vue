<template>
  <div id="app">
    <div class="navbar has-shadow">
      <div class="navbar-brand">
          <a class="navbar-item">MyCompany</a>

          <span class="navbar-burger" v-on:click="toggleNav" v-bind:class="{ 'is-active': isActive }">
            <span></span>
            <span></span>
            <span></span>
          </span>
      </div>
      <div class="navbar-menu" v-bind:class="{ 'is-active': isActive }">
        <div class="navbar-end">
          <router-link to="/" class="navbar-item r-item">Home</router-link>
          <router-link to="faq" class="navbar-item r-item">Features</router-link>
          <router-link to="faq" class="navbar-item r-item">About</router-link>
          <router-link to="faq" class="navbar-item r-item">FAQ</router-link>

          <div class="navbar-item">
            <p class="control">
              <a class="button is-primary is-outlined">
                <span class="icon">
                  <i class="fa fa-download"></i>
                </span>
                <span>Join Now</span>
              </a>
            </p>
          </div>

        </div>
      </div>
    </div>
    <router-view></router-view>

    <footer class="footer is-primary">
      <div class="container">
        <div class="columns">
          <div class="column">
            <p>Footer content goes here</p>
          </div>
          <div class="column has-text-right">
            <a class="icon" href="#"><i class="fa fa-facebook"></i></a>
            <a class="icon" href="#"><i class="fa fa-twitter"></i></a>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'app',
  data: function() {
    return {
      isActive: false
    }
  },
  methods: {
    toggleNav() {
      this.isActive = !this.isActive
    }
  }
}
</script>

<style lang="sass">
@import '../node_modules/bulma/bulma.sass'
@import 'common'

.navbar
  background-color: #383838
  a:hover
    color: gray

.navbar-brand a 
  color: #fff
  font-weight: bold

.navbar-burger span
  color: #fff
  font-weight: bold

a.r-item
  color:#C1C1C1
  padding: 0.5rem 1.75rem
  +mobile
    color: gray
    &:hover
      background-color: #F1F1F1

footer
  background-color: $primary !important
  color: #fff

  .icon
    color: #fff
    margin-left: 20px


</style>
