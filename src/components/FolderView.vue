<template>
  <div class="folder-wrapper">
    <img src="images/folder.png" alt="">
    <div @click="toogleIsShow" class="folder-block">
      <p class="folder">{{name}}</p>
      <img v-if="isShow" class="arrow" src="images/arrow.png" alt="">
      <img v-if="!isShow" class="arrow" src="images/arrow_up.png" alt="">
    </div>
    <p class="file">{{length}}</p>
  </div>
  
  <template  v-for="folder in folders">
    <div class="folder-padding" v-show="isShow">
      <FolderView :name="folder.name"  :folders="folder.folders" :files="folder.files"/>
    </div>
  </template>
  <template v-for="file in files">
    <div v-show="isShow">
      <FileView :name="file.name" :length="file.length  + 'B'" />
    </div>
  </template>
  
</template>

<script>
import FileView from "./FileView";
export default {
  name: 'FolderView',
  components: {FileView},
  props: {
    name: String,
    folders:Array,
    files:Array,
    length: String
  },
  data() {
    return {
      isShow: true
    }
  },
  methods: {
    toogleIsShow() {
      this.isShow = !this.isShow
    }
  }
}
</script>

