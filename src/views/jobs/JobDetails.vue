<template>
  <button class="backBTN" @click="back">←</button>
  <div v-if="job">
    <h1>{{job.title}}</h1>
    <h1>{{job.details}}</h1>
    <h1>job id:{{id}}</h1>
  </div>
  <div v-else> 
    loading...
  </div>
</template>

<script>
export default {
  props: ['id'],
  data() {
    return{
      job: null
    }
  },
  methods: {
    back(){
      this.$router.go(-1)
    }
  },
   mounted() {
        fetch('http://localhost:3000/jobs/' + this.id)
        .then((res) => res.json())
        .then(data => this.job = data)
        .catch(err => console.log(err.message))
    }
}
</script>

<style>
.backBTN{
  border: 2px solid #42b983;
  padding: 1em;
  background: none;
  cursor: pointer;
}
</style>