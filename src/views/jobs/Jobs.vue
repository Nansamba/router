<template>
  <div>
    <h1>jobs</h1>
    <div v-for="job in jobs" :key="job.id" class="job">
      <router-link :to="{name: 'JobDetails', params: {id: job.id }}">
         <h2>{{ job.title }}</h2>
      </router-link>
     </div>
    
  </div>
</template>

<script>
export default {
    data(){
        return {
           jobs: [
            {title: "ninja UX designer", id: 1, details: "expert in the field" },
            {title: "ninja developer", id: 2, details: "expert in the field" },
            {title: "ninja programmer", id: 3, details: "expert in the field" },
            {title: "ninja UX designer", id: 4, details: "expert in the field" },
        ]
     }}
}
</script>

<style>
.job h2{
  background: #f4f4f4;
  padding: 20px;
  border-radius: 10px;
  margin: 10px auto;
  max-width: 600px;
  cursor: pointer;
  color: #444;

}
.job h2:hover {
  background: #ddd;

}
.job a{
  text-decoration: none;
}
</style>