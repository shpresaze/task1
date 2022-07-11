<template>
  <section>
    <h1>{{ title }}</h1>
    <p>
      Со пополнето барање за одобрување на лизинг,
      <strong>профактура на добавувачот</strong> и
      <strong>прифатена лизинг понуда</strong>, потребно е да се приложат и:
    </p>
    <ul>
      <li v-for="element in myList" :key="element.title" class="ms-4">
        <p class="mb-0">
          {{ element.description }}
          <a :href="element.link">{{ element.linkedText }}</a>
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