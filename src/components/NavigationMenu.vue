<template>
  <nav class="nav-menu">
    <ul>
      <li v-for="item in items" :key="item.name">
        <a :href="item.link">{{ item.name }}</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  props: {
    items: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style>
.nav-menu ul {
  list-style-type: none;
  padding: 0;
}
.nav-menu li {
  display: inline-block;
  margin-right: 20px;
}
.nav-menu a {
  text-decoration: none;
  color: #333;
}
</style>
