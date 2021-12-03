<template>
  <div class="hello">
    <form @submit.prevent="addToSkills">
   <input type="text" placeholder="Enter your Skill" v-model="skill"/>
  </form>
    <ul>
      <li v-for="item in newskills" :key="item" >{{item}}</li>
      
    </ul>

  </div>
</template>

<script>
export default {
  name: 'Skills',
  data() {
    return{
      skill : '',
      newskills : [
        "reactjs" ,
      ],
     
      
    }
  },
  methods: {
    addToSkills(){
      this.newskills.push(this.skill)
      this.skill = ""
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >

</style>
