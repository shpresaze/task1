<template>
  <section>
    <h1>{{ title }}</h1>
    <ol>
      <li v-for="element in myList" :key="element.title" class="ms-4 fs-5">
        <p class="mb-0">{{ element.title }}</p>
        <p class="fs-6">{{ element.description }}</p>
        <p>
          <strong>{{ element.boldedDescription }}</strong>
        </p>
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