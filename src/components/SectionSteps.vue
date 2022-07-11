<template>
  <section class="container">
    <h1>{{ title }}</h1>
    <ol>
      <li v-for="step in steps" :key="step.title" class="ms-4 fs-5">
        <p class="mb-0">{{ step.title }}</p>
        <p class="fs-6">{{ step.description }}</p>
        <p>
          <strong>{{ step.description2 }}</strong>
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
      required: true,
    },
    steps: {
      type: Array,
      required: true,
    },
  },
};
</script>