<template>
  <h1></h1>
  <div v-for="project in projects" :key="project.id">
    <h1>{{ project.title }}</h1>
    <p>{{ project.description }}</p>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      projects: []
    }
  },
  methods: {
    fetchProjects() {
      axios.get('http://127.0.0.1:8000/api/project', {
        params: {
          page: 1
        }
      })
        .then(res => {
          console.log(res.data.results);
          this.projects = res.data.results.data;
        })
    }
  },
  created() {
    this.fetchProjects()
  }
}
</script>

<style></style>
