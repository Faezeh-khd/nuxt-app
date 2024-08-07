<template>
  <div>
    <header>
      <nav>
        <NuxtLink to="/">Nuxt App</NuxtLink>
        <ul>
          <li>
            <NuxtLink to="/">Home</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/about">about</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/products">products</NuxtLink>
          </li>
        </ul>
      </nav>
    </header>
    <h2>home</h2>
    <p>
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Consectetur, at!
      Ab vitae sequi consequatur explicabo pariatur quo deleniti reiciendis
      culpa?
    </p>
    <p>
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Consectetur, at!
      Ab vitae sequi consequatur explicabo pariatur quo deleniti reiciendis
      culpa?
    </p>
  </div>
</template>

<script setup></script>

<style scoped>
h2 {
  margin-bottom: 20px;
  font-size: 36px;
}
p {
  margin: 20px 0;
}
</style>
