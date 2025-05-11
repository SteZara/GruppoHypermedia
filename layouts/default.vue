<script setup lang="ts">

</script>

<template>
  <link href="https://fonts.googleapis.com/css2?family=Source+Sans+Pro:wght@300;400;600;700&display=swap" rel="stylesheet">
  <header>
    <header_content />
  </header>
  <main>
    <!-- <breadcrumb/> -->
    <NuxtPage/>
  </main>
  <footer>
    <footer_content />
  </footer>
</template>

<style scoped>

main{
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  padding: 10px; 

  /* scrollbar-width: none; */
}

header {
  top: 0;
  position: sticky;

  display: flex;    
  align-items: center;
  justify-content: space-between;

  background-color: var(--azure);
  padding: 5px;
  text-align: center;
}

footer {
  padding: 20px;
  background: linear-gradient(180deg, #3D8D8F 0%, #265559 85%);
  flex-direction: column;
}

</style>