<template>
  <!-- <h2>{{ goal }}</h2> -->
  <!-- <h2>{{ goalObj.goal }}</h2> -->
  <h2>{{ goal }}</h2>
  <!-- Task 1: Output your main course goal with help of the composition API -->
  <!-- Don't hardcode it into the template, instead hardcode it into the JS code -->
  <!-- <h3 v-if="show">{{ goal }}</h3> -->
  <!-- <h3 v-if="goalObj.show">{{ goalObj.goal }}</h3> -->
  <h3 v-if="show">{{ goal }}</h3>
  <!-- Task 2: Toggle (show/ hide) the goal with help of the button  -->
  <!-- <button @click="hideShow">Toggle Goal</button> -->
  <button @click="hideShow">Toggle Goal</button>
  <!-- Task 3: Manage data in three ways -->
  <!-- => Separate refs -->
  <!-- => Ref Object -->
  <!-- => Reactive Object -->
  <!-- Task 4: Also solve the assignment with the Options API -->
</template>

<!-- <script setup>
// import { ref } from 'vue';
import { reactive } from 'vue';

//  Separate refs
// const goal = ref('My Course Goal');
// const show = ref(false);
// Ref Object
// const goalObj = ref({
//   goal: 'My Course Goal',
//   show: false,
// });
// Reactive Object
const goalObj = reactive({
  goal: 'My Course Goal',
  show: false,
});

// function hideShow() {
//   goalObj.value.show = !goalObj.value.show;
// }

function hideShow() {
  goalObj.show = !goalObj.show;
}
</script> -->

<!-- Task 4: Also solve the assignment with the Options API -->
<script>
export default {
  data() {
    return {
      goal: 'My Course Goal',
      show: false,
    };
  },
  methods: {
    hideShow() {
      this.show = !this.show;
    },
  },
};
</script>

<style>
html {
  font-family: sans-serif;
}
body {
  margin: 3rem;
  text-align: center;
}
</style>
