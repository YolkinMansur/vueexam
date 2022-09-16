<template>
  <div>
    <ul>
      <li
        @click="item.status = !item.status"
        v-for="(item, index) in items"
        :key="index"
      >
        <p v-bind:class="{ active: item.status }">
          My name is {{ item.name }} and surname {{ item.surname }} I work at
          company called ‘{{ item.company }}’
        </p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'App',

  data() {
    return {
      items: [
        {
          name: 'John',
          surname: 'Doe',
          age: 53,
          company: 'Facebook',
          status: false,
        },
        {
          name: 'Bob',
          surname: 'Marshal',
          age: 45,
          company: 'Google',
          status: false,
        },
        {
          name: 'Joni',
          surname: 'Shepard',
          age: 38,
          company: 'Tesla',
          status: false,
        },
      ],
      isActive: true,
    };
  },
  components: {},
};
</script>

<style>
#app {
  font-family: Roboto sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #289208;
  margin-top: 60px;
}
.active {
  background-color: rgba(244, 13, 17, 0.974);
}
ul {
  list-style-type: none;
}
li {
  cursor: pointer;
}
</style>
