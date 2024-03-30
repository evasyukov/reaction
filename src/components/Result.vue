<template>
    <div>
       <h3>Результат теста:</h3>
       <p>Количество кликов: {{ clicks }}</p>
    </div>
   </template>
   
   <script>
   export default {
    name: 'Result',
    props: {
       clicks: {
         type: Number,
         required: true
       }
    }
   }
   </script>