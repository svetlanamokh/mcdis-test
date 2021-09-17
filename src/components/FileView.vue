<template>
  <table class="file-content">
    <tr>
      <td>
        <img src="/images/file.png" alt="">
      </td>
      <td>
        <p class="file">{{name}}</p>
      </td>
      <td class="file-length">{{length}}</td>
    </tr>
  </table>
</template>

<script>
export default {
  name: 'FileView',
  props: {
    name: String,
    length: String
  }
}
</script>


