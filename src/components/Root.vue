<template lang="pug">


.targets
  div.js-target
    h1 Javascript Target
    span.big(@click) 'js-target'

  div.root
    h1 Root Target
    span.big 'root'

  div.counter1
    h1 Counter Target
    span.big 'counter1'
 
  div.counter2
    h1 Counter Target
    span.big 'counter2'
 
  div.counter3
    h1 Counter Target
    span.big 'counter3'
 
  div.counter4
    h1 Counter Target
    span.big 'counter4'

  //- #syntaxExamples.syntaxExamples
  //-   div.classOne.classTwo
  //-     | text inside a div with 'classOne' and 'classTwo'

</template>

<script>
export default {
    //- components: { Icon },

    //- props: {
    //-   grade: {
    //-     type: Number,
    //-     required: true
    //-   },
    //-   maxStars: {
    //-     type: Number,
    //-     default: 5
    //-   },
    //-   hasCounter: {
    //-     type: Boolean,
    //-     default: true
    //-   }
    //- },

    //-   data() {
    //-     return {
    //-       stars: this.grade
    //-     }
    //-   },

    //-   methods: {
    //-     rate(star) {
    //-       if (
    //-         typeof star === 'number' &&
    //-         star <= this.maxStars &&
    //-         star >= 0
    //-       )
    //-         this.stars = this.stars === star ? star - 1 : star
    //-     }
    //-   }
     }
</script>

<style lang="scss">
    body{
      text-align:center;
    }
    .targets {
      display : grid;

      grid-template-areas : 
      "root root  js-target js-target  "
      "counter1  counter1      counter2     counter2  "
      "counter3  counter3      counter4     counter4  ";
      grid-template-columns : [col-1] 25% [col-2] 25% [col-3] 25% [col-4] 25%;
      grid-template-rows : 35vh 35vh 35vh;


      .big {
        font-size : 1.4rem;
        display : block;
        margin-top : 1rem;
        width:20rem;
        margin: auto;
        margin-top:1rem;
        border-radius:.5rem;
        box-shadow:
        3px 0px 6px 0px rgba(0,0,0,0.4), 
        -3px 0px 6px 0px rgba(0,0,0,0.4);
      
      }
    }

    .root {
      grid-area : root;
    }

    .js-target {
      grid-area : js-target;
    }

    .counter1{
      grid-area : counter1;

    }

    .counter2{
      grid-area : counter2;

    }

    .counter3{
      grid-area : counter3;

    }

    .counter4{
      grid-area : counter4;

    }
</style>
