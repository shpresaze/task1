<template>
  <section class="container">
    <h1>{{ title }}</h1>
    <p>
      Со пополнето барање за одобрување на лизинг,
      <strong>профактура на добавувачот</strong> и
      <strong>прифатена лизинг понуда</strong>, потребно е да се приложат и:
    </p>
    <ul>
      <li v-for="document in documents" :key="document.title" class="ms-4">
        <p class="mb-0">
          {{ document.description }}
          <a :href="document.link"
            ><strong>{{ document.linkedText }}</strong></a
          >
        </p>
      </li>
    </ul>
    <p>
      <strong
        >Документација треба да биде заверена со потпис и печат на овластеното
        лице!
      </strong>
    </p>
    <p>
      <strong>AUTOWELT</strong> го задржува правото да побара дополнителна
      документација за разгледување на барањата за одобрување на лизинг.
    </p>
    <hr />
  </section>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: false,
    },
    documents: {
      type: [],
      required: true,
    },
  },
};
</script>