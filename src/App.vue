<template>
  <div id="app">
    <Map :data="data_oggi" />
    <DateTimePicker @pickedDate="updatedDatePicker" @pickedTime="updatedTimePicker"/>
  </div>
</template>

<script>
import Map from "./components/Map";
import DateTimePicker from "./components/DateTimePicker";
export default {
  name: 'App',
  components: {
    Map,
    DateTimePicker
  },
  data() {
    return {
      data_di_oggi: new Date(),
      data_oggi: [],
    }
  },
  mounted() {
      var i = 1;
      var f = () => {
          this.data_oggi.push(i);
          i = i+1;
          setTimeout(f, 3000);
      };
      f();
  },
  methods: {
    updatedDatePicker(newDate) {
      console.log("App value recieved date: " + newDate);
    },
    updatedTimePicker(newTime) {
      console.log("App value recieved time: " + newTime);
    }
  },
}
</script>