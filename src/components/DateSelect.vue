<template>
  <div class="date-select">
    <link rel="import" href="static/bower_components/vaadin-date-picker/vaadin-date-picker.html">
    <vaadin-date-picker
        :label="label"
        :value="date"
        v-on:value-changed="onDateChange">
    </vaadin-date-picker>
  </div>
</template>

<script>
export default {
  data () {
    return {
      label: 'Select a date',
      date: '2016-12-31'
    }
  },
  methods: {
    onDateChange: function (e) {
      console.log('date changed: ' + e.detail.value)
    }
  }
}
</script>