<template>
  <div class="container">
    <h1>Belajar Components, Props, Emits, dan Slots</h1>

    <MyButton 
      buttonText="Klik disini!" 
      @customClick="handleClick"
    >
      <template #default>
        <strong> - Slot: Ini isi dari induk - </strong>
      </template>
    </MyButton>

    <p class="message">{{ message }}</p>
  </div>
</template>

<script>
import MyButton from './components/MyButton.vue'

export default {
  components: {
    MyButton
  },
  data() {
    return {
      message: 'Belum diklik'
    }
  },
  methods: {
    handleClick() {
      this.message = 'Tombol diklik! Kamu keren!'
    }
  }
}
</script>

