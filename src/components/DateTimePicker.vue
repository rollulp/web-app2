<template>
    <div>
        <datetime format="YYYY/MM/DD" width="300px" @input="updatedCalendar" firstDayOfWeek="1" />
        <!--<VueSlideBar
        v-model="slider.value"
        :data="slider.data"
        :range="slider.range"
        :labelStyles="{ color: '#003300', backgroundColor: '#003300' }"
        :processStyle="{ backgroundColor: 'green' }"
        @callbackRange="updatedSlider">
        </VueSlideBar> -->
    </div>
</template>

<script>
import datetime from 'vuejs-datetimepicker';
//import VueSlideBar from 'vue-slide-bar';
export default {
  name: 'DateTimePicker',
  components: {
      datetime,
      //VueSlideBar
  },
  props: {
      data: Array,
  },
  mounted() {
  },
  updated() {
  },
  methods: {
    updatedCalendar(newDate) {
        console.log("DatePicker::UpdatedCalendar val recieved::" + newDate);
        this.$emit("pickedDate", newDate)
    },
   /* updatedSlider(newTime) {
        console.log("Slider::updatedSlider new val: " + JSON.stringify(newTime) );
        //this.$emit("pickedTime", this.);
    }*/
  }
}
</script>