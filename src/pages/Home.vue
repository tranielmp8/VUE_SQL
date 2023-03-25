<template>
  <div class="home">
    <Hero />
    <h4>Below is where the magic happens. I have created many different tabs that show SQL queries if you click on the TITLE in the tabs</h4>
    <p class="anime">Yes I am a nerd so the tables I created were anime shows I watched when I was younger. (Naruto and Bleach)</p>
    <div class="project">
      <div v-for="post in posts" key="post.id" >
        <DataList  :post="post"/>
      </div>
    </div>
  </div>
</template>

<script>
import DataList from '../components/DataList.vue'
import Hero from '../components/Hero.vue';
import { ref } from 'vue';
  export default {
    components: {DataList, Hero},
    setup(){
      const posts = ref([
      {
      "id": 1,
      "img": "/src/assets/images/create_table.png",
      "title": "Create Database Table",
      "code": "CREATE TABLE naruto(id SERIAL PRIMARY KEY,name VARCHAR(50),village VARCHAR(50),power VARCHAR(50),age INTEGER, rank VARCHAR(50))"
      },
      {
        "id": 2,
        "img": "/src/assets/images/insert1.png",
        "title": "Insert data into table",
        "code": "INSERT INTO naruto(name, village, power, age, rank)values ('naruto','leaf','shadow clone',12,'genin')"
      },
      {
      "id": 3,
      "title": "Insert multiple lines of values",
      "img": "/src/assets/images/insert2.png",
      "code": "INSERT INTO naruto(name, village, power, age, rank)\nvalues\n('jiraiya', 'leaf', 'rasengan', 50, 'sage'),\n('sakura', 'leaf', 'creation rebirth', 12, 'genin'),\n('gaara', 'sand', 'sand binding coffin', 12, 'jinchuriki'),\n('kankuro', 'sand', 'salamander', 12, 'genin'),\n('temari', 'sand', 'dust wind technique', 12, 'genin'),\n('zabuza', 'mist', 'water prison technique', 26, 'anbu'),\n('kisame', 'mist', 'five feeding sharks', 29, 'jounin'),\n('killer bee', 'cloud', 'tailed beast ball', 36, 'jinchuriki'),\n('darui', 'cloud', 'black panther', 26, 'jounin')"
      },
      {
      "id": 4,
      "title": "Selecting all columns/fields from table",
      "code": "Select * From naruto"
      },
      {
        "id": 5,
        "title": "Selecting select columns/fields from table",
        "code": "Select name, village From naruto"
      }
    ])
      
      // const load = async () => {
      //   try {
      //     let data = await fetch('http://localhost:3000/data')
      //     if(!data.ok){
      //       throw Error('no data available')
      //     }
      //     posts.value = await data.json()
      //   } catch (err) {
      //     console.log(err.message)
      //   }
      // }

      // load()

      return { posts }
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
</style>