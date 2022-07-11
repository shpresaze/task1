<template>
  <section>
    <h1>{{ title }}</h1>
    <ol>
      <li v-for="element in myList" :key="element.title">
        <p class="mb-0 fs-5">{{ element.title }}</p>
        <p>{{ element.description }}</p>
        <p>{{ element.boldedDescription }}</p>
      </li>
    </ol>
  </section>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: false,
    },
    myList: {
      type: [],
      required: true,
    },
  },
};
</script>