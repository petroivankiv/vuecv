<template>
  <header>
    <img src="../assets/photo.png" alt="My Photo">
    <div class="header-profile">
      <span class="header-profile_name">{{ name }}</span>
      <span>{{ position }}</span>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  props: {
    name: String,
    position: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header {
  display: flex;
  align-items: center;
  justify-content: flex-start;
}

img { height: 100px; border-radius: 15%; }

.header-profile {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  margin-left: 20px;
}

.header-profile_name {
  font-size: 32px;
  font-weight: bold;
}
</style>
