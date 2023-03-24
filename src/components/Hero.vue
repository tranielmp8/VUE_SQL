<template>
  <div>
    <h1>SQL Sheet of Knowledge</h1>
    <p>Structured query language (SQL) is a programming language for storing and processing information in a relational database</p>
    <p>SQL is an important skill to have if you are a DataAnalyst or want to be one.</p>
    <p>I have created a simple webpage with SQL basics you should know using PostgreSQL</p>
    <div>
      <h3>Getting started with Postgres</h3>
      <h3>
        <a href="https://www.postgresql.org/download/" target="_blank">Download PostgreSQL</a>
      </h3>
      <p>make sure to choose your correct operating system before downloaded</p>
      <img src="../assets/images/postgres_download.png" alt="postgres" >
      <h3>NOTE: when downloading postgreSQL you will be prompted to create a password. WRITE IT DOWN</h3>
      <p>To get the postgresAdmin app please click link below</p>
      <h3><a href="https://www.pgadmin.org/download/" target="_blank">PGAdmin</a></h3>
      <img class="pgadmin" src="../assets/images/pgadmin.png" alt="pgadmin">
      <h3>NOTE: you will be prompted to create another password. It can be the same, but REMEMBER THE PASSWORD.  </h3>
    </div>
  </div>
</template>

<script>
  export default {
    setup(){


      return{  }
    }
  }
</script>

<style>
.pgadmin {
  max-width: 700px;
}

</style>