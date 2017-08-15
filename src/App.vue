<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>{{msg}}</h1>
    <h3 v-text="text"></h3>
    <div v-html='htmltxt'></div>
    <input v-model="newitem" class="input" v-on:keyup.enter="additem()">
    <ui>
      <li v-for = "item in items"  v-bind:class = "{isfinished:item.isfinished}"  v-on:click="doThis(item)">
        {{item.label}}
      </li>
    </ui>
  </div>
</template>

<script>
export default {
  name: 'app',
  data(){
    return{
       msg:'this is my first vue project',
       text:'this is a text',
       htmltxt:'<span>this is a txt in html </span> <strong>but it is a false.</strong>',
       items:[
           {label:'coding',
           isfinished:true},
           {label:'waking',
           isfinished:false}
       ],
       newitem:'',
    }
  },
  methods: {
    doThis:function (item) {
      item.isfinished=!item.isfinished
      console.log(item.isfinished)
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
  font-size: 25px;
}
span{
  font-size: 20px;
  color: red;
  font-weight: bold;
}
.isfinished{
  text-decoration: underline;
}
</style>
