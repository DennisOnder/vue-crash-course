<template>
  <div class="hello">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in skills" :key="index">{{ index }}. {{ data.skill }}</li>
        <p v-if="(skills.length) >= 1">You have more than one skill.</p>
        <p v-else>You have less than one skill.</p>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Skills",
  data() {
    return {
      skills: [
        {
          skill: "Vue.js"
        },
        {
          skill: "React.js"
        },
        {
          skill: "Angular"
        }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
