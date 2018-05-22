<template>
  <div class="calendar-input">
    <input class="input-box"
           type="text"
           readonly="true" 
           v-model="date"
           @click="showPicker"
    >
    <date-picker ref="datePicker" :showFlag="isShowPicker" @sendDate="setDate"></date-picker>
  </div>
</template>

<script>
import DatePicker from 'components/date-picker'

export default {
  name: 'CalendarInput',
  components: {
    DatePicker
  },
  data() {
    return {
      isShowPicker: false,
      date: ''
    }
  },
  methods: {
    showPicker() {
      this.isShowPicker = !this.isShowPicker
    },

    setDate(val) {
      this.date = val
    }
  },
  created() {
    this.showPicker()
  }
}
</script>

<style lang="scss" scoped>
.calendar-input {
  width: 24rem;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);

  .input-box {
    display: block;
    box-sizing: border-box;
    width: 100%;
    text-align: center;
    padding: 1rem;
    font-size: 1.2rem;
    border: 1px solid #ccc;
    outline: none;
    cursor: pointer;
  }
}
</style>