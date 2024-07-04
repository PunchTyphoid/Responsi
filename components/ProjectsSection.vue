<template>
   <link rel='stylesheet' href='https://cdn.jsdelivr.net/npm/bootstrap@4.4.1/dist/css/bootstrap.min.css'>
  <section class="projects">
    <nav>
      <section class="nav-section">
            <a><NuxtLink to="/" class="nav-item">Home</NuxtLink></a>
            <a><NuxtLink to="/about" class="nav-item">About</NuxtLink></a>
            <a><NuxtLink to="/contact" class="nav-item">Contact</NuxtLink></a>
            <a><NuxtLink to="/projects" class="nav-item">Projects</NuxtLink></a>
      </section>
    </nav>
    <h2>My Projects</h2>
    Pembuatan Website Portofolio
    <br>
    <img src="/assets/P2.png"  width="950">
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    Pembuatan Section Our Service Pada Website
    <br>
    <img src="/assets/P3.png"  width="950">
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    Bug Hunting
    <br>
    <img src="/assets/P1.jpg"  width="950">
  </section>
</template>

<script>
export default {
  name: 'ProjectsSection'
}
</script>

<style scoped>
.projects {
  text-align: center;
  padding: 100px 0;
  background-image: url(@/assets/bg.jpeg);
}
</style>
