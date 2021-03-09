<template>
    <div>
        <p>ciao {{data}} </p>
        <p v-for="d in data" :key="d"> {{d}}</p>

    </div>
</template>

<script>
export default {
  name: 'Map',
  props: {
      data: Array,
  },
  components: {
  },
  mounted() {
  },
  updated() {
      //console.log("UPDATED");
  },
  methods: {

  }
}
</script>