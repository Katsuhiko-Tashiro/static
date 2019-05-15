<template>
  <v-layout
    column
    justify-center
    align-center
  >
    <v-flex>
        <v-btn @click.stop="onSizeSelected">サイズを選ぶ</v-btn>
        <v-btn @click.stop="onClickPayment">リクエストをする</v-btn>
    </v-flex>
    <v-flex v-if="selected" id="selected">
        <a href="">サイズを選んだよ</a>
    </v-flex>
    <v-flex v-if="requested" id="requested">
        <a href="">リクエストをしたよ</a>
    </v-flex>
  </v-layout>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo
  },
  data() {
    return {
    selected: false,
    requested: false
    }
  },
  methods: {
    onSizeSelected() {
      this.selected = true
    },
    onClickPayment() {
      this.requested = true
    }
  }

}
</script>
