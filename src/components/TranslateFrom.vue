<template>
  <div id="translateFrom" class="row">
    <div class="col-md-6 col-md-offset-3">
      <form id="transFrom" class="well form-inline" v-on:submit='fromSubmit'>
        <input class="form-control" v-model='textToTranslate' type="text" placeholder="输入需要翻译的内容">
        <select class="form-control" v-model='language'>
          <!-- <option value="en">English</option> -->
          <option v-for="todo in todos" v-bind:value= 'todo.name' >
            {{ todo.text }}
          </option>
        </select>
        <input class="btn btn-primary" type="submit" value="翻译">
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'translateFrom',
  data:function(){
    return {
      todos: [
        { "name": "az" , "text" :  "Azerbaijan"},
        { "name": "sq" , "text" :  "Albanian"},
        { "name": "am" , "text" :  "Amharic"},
        { "name": "en" , "text" :  "English"},
        { "name": "ar" , "text" :  "Arabic"},
        { "name": "hy" , "text" :  "Armenian"},
        { "name": "af" , "text" :  "Afrikaans"},
        { "name": "eu" , "text" :  "Basque"},
        { "name": "ba" , "text" :  "Bashkir"},
        { "name": "be" , "text" :  "Belarusian"},
        { "name": "bn" , "text" :  "Bengali"},
        { "name": "my" , "text" :  "Burmese"},
        { "name": "bg" , "text" :  "Bulgarian"},
        { "name": "bs" , "text" :  "Bosnian"},
        { "name": "cy" , "text" :  "Welsh"},
        { "name": "hu" , "text" :  "Hungarian"},
        { "name": "vi" , "text" :  "Vietnamese"},
        { "name": "ht" , "text" :  "Haitian (Creole)"},
        { "name": "gl" , "text" :  "Galician"},
        { "name": "nl" , "text" :  "Dutch"},
        { "name": "mrj" , "text" :  "Hill Mari"},
        { "name": "el" , "text" :  "Greek"},
        { "name": "ka" , "text" :  "Georgian"},
        { "name": "gu" , "text" :  "Gujarati"},
        { "name": "da" , "text" :  "Danish"},
        { "name": "he" , "text" :  "Hebrew"},
        { "name": "yi" , "text" :  "Yiddish"},
        { "name": "id" , "text" :  "Indonesian"},
        { "name": "ga" , "text" :  "Irish"},
        { "name": "it" , "text" :  "Italian"},
        { "name": "is" , "text" :  "Icelandic"},
        { "name": "es" , "text" :  "Spanish"},
        { "name": "kk" , "text" :  "Kazakh"},
        { "name": "kn" , "text" :  "Kannada"},
        { "name": "ca" , "text" :  "Catalan"},
        { "name": "ky" , "text" :  "Kyrgyz"},
        { "name": "zh" , "text" :  "Chinese"},
        { "name": "ko" , "text" :  "Korean"},
        { "name": "xh" , "text" :  "Xhosa"},
        { "name": "km" , "text" :  "Khmer"},
        { "name": "lo" , "text" :  "Laotian"},
        { "name": "la" , "text" :  "Latin"},
        { "name": "lv" , "text" :  "Latvian"},
        { "name": "lt" , "text" :  "Lithuanian"},
        { "name": "lb" , "text" :  "Luxembourgish"},
        { "name": "mg" , "text" :  "Malagasy"},
        { "name": "ms" , "text" :  "Malay"}
      ],
      textToTranslate:'',
      language:''
    };
  },
  methods: {
    fromSubmit:function(e) {
      // alert(this.language);
      // console.log(this.todos[2].name);
      this.$emit('formSubmit', this.textToTranslate, this.language);
      e.preventDefault();
    }
  },
  created:function(){
    this.language = 'en';
  }
}
</script>

<style>
#transFrom{
  border: 1px solid #ccc;
  border-radius: 10px;
}
</style>
