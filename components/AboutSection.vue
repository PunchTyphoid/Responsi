<template>
  <section class="about">
    <nav>
      <section class="nav-section">
            <a><NuxtLink to="/" class="nav-item">Home</NuxtLink></a>
            <a><NuxtLink to="/about" class="nav-item">About</NuxtLink></a>
            <a><NuxtLink to="/contact" class="nav-item">Contact</NuxtLink></a>
            <a><NuxtLink to="/projects" class="nav-item">Projects</NuxtLink></a>
      </section>
    </nav>
    <h2>About Me</h2>
    <link rel='stylesheet' href='https://cdn.jsdelivr.net/npm/bootstrap@4.4.1/dist/css/bootstrap.min.css'>
    <img src="/assets/PP.png" alt="Photo" class="rounded-circle" width="365">
    <p>I am a cybersecurity junior who is more inclined towards the red team.</p>
    <p>I Master several methods such as SQL injection, XSS, and many more</p>
    <p>I also have an interest in fortend development.</p>
  </section>
</template>

<script>
export default {
  name: 'AboutSection'
}
</script>

<style scoped>
.about {
  text-align: center;
  padding: 100px 0;
  background-image: url(@/assets/bg.jpeg);
}
</style>
