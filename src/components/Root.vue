<template lang="pug">
div.container

  div.interior.one
  div.interior.two
  div.interior.three
  div.interior.four
  div.interior.five
  
</template>

<script>
export default {


       data() {
         return {
           
         }
       },
         computed: {
    fullName: {
      // getter
      get: function () {
        return this.firstName + ' ' + this.lastName
      },
      // setter
      set: function (newValue) {
        var names = newValue.split(' ')
        this.firstName = names[0]
        this.lastName = names[names.length - 1]
      }
    }
  },
       methods: {
       
         ಠ(){
           
       }
     }
}
</script>

<style lang="scss">
 body{
    margin:0;
}
.container{
  display:grid;
  // grid-template-columns : 12% auto 400px 12%;         
  grid-template-columns : 20vw 20vw 20vw 20vw 20vw;       
  grid-template-rows : 20vh 20vh 20vh 20vh 20vh ;  //5 columns y axis

}
.interior{
  // background-color:rgba(41, 97, 188,0.3)
}
.one{
  background-color:rgba(188, 41, 53, 0.3);
  grid-column: 1/2;  //x axis      
  grid-row: 1/2;     //y axis
}
.two{
  background-color:rgba(41, 188, 41, 0.3);
  grid-column: 2/3;  //x axis
  grid-row: 2/3;     //y axis
}
.three{
  background-color:rgba(166, 188, 41, 0.3);
  grid-column: 3/4;  //x axis
  grid-row: 3/4;     //y axis 
}
.four{
  background-color:rgba(188, 41, 156, 0.3);
  grid-column: 4/5;  //x axis
  grid-row: 4/5;     //y axis 
}
.five{
  background-color:rgba(41, 97, 188,0.3);
  grid-column: 5/6;  //x axis
  grid-row: 5/6;     //y axis 
}
</style>
