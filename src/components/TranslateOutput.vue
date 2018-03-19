<template>
  <div id="translateOutput" class="Output">
      <h2>{{translatedText}}</h2>
  </div>
</template>

<script>

export default {
  name: 'translateOutput',
  props:[
    'translatedText'
  ]
}
</script>

<style>
  .Output{
    font-size: 36px;
  }
</style>
