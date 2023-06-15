<template>
<div class="card__wrapper">
  <div class="card__content">{{ dataProps.name }}</div>
  <div class="card__content">
  <iconMoney class="card__icon"></iconMoney>
  <span class="card__content-subtitle">{{ dataProps.profit }}</span>
  </div>
</div>
</template>


<script>

import iconMoney from './iconMoney.vue'

export default {
  name: 'ItemCardComponent',
  components: {
    iconMoney
  },
  props: {
      dataProps: {
        type: Object,
        default: () => ({}),
      },
  },
  data() {
    return {
      shops: [        ]
    }
  }
}
</script>

<style>
.card__wrapper {
  margin-right: 10px;
  max-width: 190px;
  min-height: 130px;
  width: 100%;
  border-radius: 18px;
  border: 1px solid rgba(222, 195, 255, 0.18);
  box-shadow: 0px 5px 7px -2px rgba(222, 195, 255, 0.18);
  background-color: #ffffff;
}
.card__content {
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 12px;
  font-size: 18px;
  color:#9eafe0;
}
.card__content-subtitle {
  font-size: 34px;
  color: #191651;
}
.card__icon {
  margin-right: 8px;
  color: #191651;
}
</style>