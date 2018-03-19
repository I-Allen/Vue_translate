<template>
  <div id="app">
    <h1 class="text-danger">Vue在线翻译</h1>
    <h4 class="text-muted" >简单 / 易用 / 便捷</h4>
    <h3 class="text-inof">张铭钦</h3>
    <h5 class="text-inof">我的博客: <a class="text-warning" href="http://zmqblog.top/">http://zmqblog.top/</a></h5>
    <h5 class="text-inof">我的GitHub: <a class="text-warning" href="https://github.com/MeetZhang">https://github.com/MeetZhang</a></h5>
    <translateFrom v-on:formSubmit='translateText'></translateFrom>
    <translateOutput v-text='translatedText'></translateOutput>
  </div>
</template>

<script>
import TranslateFrom from './components/TranslateFrom'
import TranslateOutput from './components/translateOutput'


export default {
  name: 'app',
  data:function(){
    return{
      translatedText:''
    }
  },
  components:{
    TranslateFrom,TranslateOutput
  },
  methods:{
    translateText:function(text,language){
      // alert(text)
      this.$http.get('https://translate.yandex.net/api/v1.5/tr.json/translate?key=trnsl.1.1.20171017T114411Z.2ca59c587b856e87.800293e16cde7a6ebbb08cd4f77f672184303c4f&lang=' + language + '&text=' + text)
      .then((response)=>{
        // console.log(response.body.text[0]);
        this.translatedText = response.body.text[0];
      })

    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
