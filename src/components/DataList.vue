<template>
  <div >
    <div class="actions" >
      <h3 @click="showDetails = !showDetails"> {{ post.title }} </h3>
    </div>
    <div v-if="showDetails" class="details">
      <img :src="post.img" alt="">
      <code> {{ post.code }} </code>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
  export default {
    props: ['post'],
    setup() {
      const showDetails = ref(false)
      
      
      return {showDetails}
    }
  }
</script>

<style scoped>

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
    transition: .3s ease-in;

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