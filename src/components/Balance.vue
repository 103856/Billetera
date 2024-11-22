<template>
  <div :class="['balance', total >= 0 ? 'positive' : 'negative']">
    Your Balance: ${{ total }}
  </div>
</template>

<script setup>
defineProps({
  total: Number
});
</script>

<style scoped>
.balance {
  font-size: 24px;
  font-weight: bold;
  margin-top: 20px;
}

.balance.positive {
  color: #2ecc71;  /* Verde para saldo positivo */
}

.balance.negative {
  color: #e74c3c;  /* Rojo para saldo negativo */
}
</style>
