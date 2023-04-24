<template>
    <div>
      <h2>Hello {{ name }} a.ka.a {{ heroName }}</h2>
    </div>
  </template>
  
  <script>
  export default {
    name: 'UserGreeting',
    props: ['name', 'heroName'] 
  }
  </script>
  