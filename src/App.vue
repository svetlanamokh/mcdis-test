<template>
  
  <div class="wrapper">
    <h1>Storage</h1>
    <div class="wrapper-content">
      <div>
        <FolderView name="project" :folders="folders" :files="files" />
      </div>
      <div class="diagram">
        <img src="/images/illustration.jpg">
        <div class="diagram-lines">
          <div class="diagram-lines-one">
            <div class="first"></div>
            <p>svg, <span>4KB</span></p>
          </div>
          <div class="diagram-lines-two">
            <div class="second"></div>
            <p>jpg, <span>3KB</span></p>
          </div>
          <div class="diagram-lines-three">
            <div class="third"></div>
            <p>js, <span>50KB</span></p>
          </div>
        </div>
      </div>
      
    </div>
  </div>

</template>

<script>
import FolderView from './components/FolderView.vue'
import data from './data/list';

export default {
  name: 'App',
  components: {
    FolderView
  },
  data: () => data
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
