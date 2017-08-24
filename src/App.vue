<template>
  <div id="app">
    <img src="./assets/logo.png">
<<<<<<< HEAD
    <hello></hello> 
    <h2 v-html="title"></h2>
=======
   <!--  <hello></hello> -->
     <h2 v-html="title"></h2>
>>>>>>> 1ade82b98b89ee6a96dbc0ea07782801988d9789
     <h1 v-text="msg"></h1>
     <input v-model="newitem" v-on:keyup.enter="additem()">
     <ul>
       <li v-for="item in items" v-bind:class="{finished: item.isfinished }" v-on:click="dothis(item)">
       {{item.label}}
       </li>
     </ul>
  </div>
</template>

<script>
// import Hello from './components/Hello'

export default {
  name: 'app',
  // components: {
  //   Hello
  // },
   data () {
    return {
      title: '<strong>todo LIST</strong>',
      msg:"This is my first vue project is numberone",
      items:[
<<<<<<< HEAD
          {label:'coding',
          isfinished: false
          },
          {label:'waking',
          isfinished: true
          },  
=======
>>>>>>> 1ade82b98b89ee6a96dbc0ea07782801988d9789
      ],
      newitem:'',
    }
  },
  methods: {
    dothis: function (item) {
       item.isfinished = !item.isfinished
    },
    additem:function(){
        this.items.push({
          label:this.newitem,
          isfinished:true
        })
        this.newitem=''
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
h1, h2 {
  font-weight: normal;
}
.finished{
  text-decoration: underline !important;
}
<<<<<<< HEAD

=======
li{
  list-style: none;
  text-align: center;
  border: 5px solid red;
  margin: 1px auto;
}
ul{
  border: 5px solid blue;

}
>>>>>>> 1ade82b98b89ee6a96dbc0ea07782801988d9789
</style>
