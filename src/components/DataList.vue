<template>
  <div class="project">
    <h4>Below is where the magic happens. I have created many different tabs that show SQL queries if you click on the TITLE in the tabs</h4>
    <p class="anime">Yes I am a nerd so the tables I created were anime shows I watched when I was younger. (Naruto and Bleach)</p>
    
    <div v-for="d in data" :key="d.id" >
      <div class="actions" >
        <h3 @click="showDetails = !showDetails"> {{ d.title }} </h3>
      </div>
      <div v-if="showDetails" class="details">
        <code> {{ d.code }} </code>
      </div>
    </div>
  </div>
</template>

<script>

import { ref } from 'vue'; 
  export default {
    setup() {

      let showDetails = ref(false)
      const data = ref([
      {
      "id": 1,
      "title": "CREATE DATABASE TABLE",
      "code": `CREATE TABLE naruto(\n
      id SERIAL PRIMARY KEY,\n
      name VARCHAR(50),\n
      village VARCHAR(50),\n
      power VARCHAR(50),\n
      age INTEGER,\n
      rank VARCHAR(50)\n
      )\n
    `
      },
      {
      "id": 2,
      "title": "INSERT VALUES IN TABLES",
      "code": `INSERT INTO naruto(name, village, power, age, rank)
      values (
        'naruto',
        'leaf',
        'shadow clone',
        12,
        'genin'
      )\n
    `
      },
      {
      "id": 2,
      "title": "INSERT VALUES IN TABLES",
      "code": `INSERT INTO naruto(name, village, power, age, rank)
      values (
        'naruto',
        'leaf',
        'shadow clone',
        12,
        'genin'
      )\n
    `
      },
    ])


      return {data, showDetails}
    }
  }
</script>

<style scoped>
  .project {
    margin: 20px auto;
    background: white;
    padding: 10px 20px;
    border-radius: 4px;
    box-shadow: 1px 2px 3px rgba(0,0,0,0.05);
    border-radius: 7px;
    
  }

  h3 {
    cursor: pointer;

  }
  
  .anime {
    border-bottom: solid #333 10px;
    padding: .5rem;
  }
  .actions {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    border-radius: 7px;
    padding: .7rem;
    background: #333;
    color: #fff;
    box-shadow: 5px 7px 7px rgba(233, 4, 4, 0.438);
    margin: 1rem auto;

  }

  .details {
    display: flex;
    flex-direction: column;
  }

  code {
    text-align: center;
    padding: .7rem;
  }
  /* .material-icons {
    font-size: 24px;
    margin-left: 10px;
    color: #bbb;
    cursor: pointer;
  }
  .material-icons:hover {
    color: #777;
  } */
  /* completed projects */
  /* .project.complete {
    border-left: 4px solid #00ce89;
  } */
  /* .project.complete .tick {
    color: #00ce89;
  } */
</style>