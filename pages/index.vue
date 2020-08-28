<template>
  <div class="flex-container">
    <div>
      <CryptoIcon name="btc" />
    </div>
    <div>
      <CryptoIcon name="eth" />
    </div>
    <div>
      <CryptoIcon name="usdt" />
    </div>
    <div>
      <CryptoIconMana />
    </div>
    <div v-for="name in iconNames" :key="`icon-${name}`">
      <CryptoIcon :name="name" />
    </div>
  </div>
</template>

<script>
import CryptoIconMana from 'cryptocurrency-icons/svg/color/mana.svg?inline'

export default {
  components: {
    CryptoIconMana,
  },
  data() {
    return {
      iconNames: [
        'xrp',
        'link',
        'bch',
        'ltc',
        'bsv',
        'bnb',
        'fsn',
        'ftc',
        'fuel',
        'fun',
        'gin',
        'glxt',
      ],
    }
  },
}
</script>

<style>
.flex-container {
  display: flex;
  flex-wrap: wrap;
  padding: 1.5rem 0 1.5rem 1.5rem;
  max-width: 48rem;
  margin: 0 auto;
}
.flex-container div {
  padding: 1rem;
  margin: 0 1.5rem 1.5rem 0;
  border-radius: 0.5rem;
  background: #fff;
  box-shadow: 0 0.325rem 1rem -0.25rem rgba(15, 25, 42, 0.1),
    0 0.25rem 0.325rem -0.125rem rgba(15, 25, 42, 0.05);
}
</style>
