<template>
  <div class="index container">
    <div class="card" v-for="course in courses" :key="course.id">

      <div class="card-content">
      
      <h2 class="indigo-text"> {{ course.title }} </h2>
      <ul class="ingredients">
        <li v-for="(ing, index) in course.ingredients" :key="index"> 
          <span class="chip"> {{ ing }} </span>
        </li>
      </ul>
    </div>
    </div>
    
    
    
  </div>
</template>

<script>
export default {
  name: 'Index',
  data() {
    return {
      courses: [
        { title: 'Node Basics', slug: 'node-basics', ingredients: ['node', 'express', 'javascript'], id: '1'},
        { title: 'PHP Basics', slug: 'php-basics', ingredients: ['php', 'apache', 'MySql'], id: '2'},

      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
