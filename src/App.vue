<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
              <button @click="selectedComponent='app-quote'">Quotes</button>
              <button @click="selectedComponent='app-author'">Author</button>
              <button @click="selectedComponent='app-new'">New</button>
              <p>{{ selectedComponent }}</p>
              <hr>
              <keep-alive>
                 <component :is="selectedComponent"> 
                <p>Quotes component</p>
              </component>
              </keep-alive>
             
               <!-- <app-quote>
                 <h2 slot="title">{{ title }}</h2>
                 <p slot="content">wonderful quotes here!!</p>
               </app-quote> -->
            </div>
        </div>
    </div>
</template>

<script>
import quote from './components/Quote.vue';
import New from './components/New.vue';

import Author from './components/Author.vue';

    export default {
      data:function(){
        return{
          title:'Quotes',
          selectedComponent:'appQuote'
        }
      },
        components:{
          appQuote:quote, 
          appNew:New,
           appAuthor:Author
        }
       
    }
</script>

<style>
</style>