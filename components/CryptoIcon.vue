<template functional>
  <component :is="$options.cryptoIconComponent(props.name)" />
</template>

<script>
const cryptoIcons = {
  bch: require('cryptocurrency-icons/svg/color/bch.svg?inline'),
  bnb: require('cryptocurrency-icons/svg/color/bnb.svg?inline'),
  bsv: require('cryptocurrency-icons/svg/color/bsv.svg?inline'),
  btc: require('cryptocurrency-icons/svg/color/btc.svg?inline'),
  eth: require('cryptocurrency-icons/svg/color/eth.svg?inline'),
  fsn: require('cryptocurrency-icons/svg/color/fsn.svg?inline'),
  ftc: require('cryptocurrency-icons/svg/color/ftc.svg?inline'),
  fuel: require('cryptocurrency-icons/svg/color/fuel.svg?inline'),
  fun: require('cryptocurrency-icons/svg/color/fun.svg?inline'),
  gin: require('cryptocurrency-icons/svg/color/gin.svg?inline'),
  glxt: require('cryptocurrency-icons/svg/color/glxt.svg?inline'),
  link: require('cryptocurrency-icons/svg/color/link.svg?inline'),
  ltc: require('cryptocurrency-icons/svg/color/ltc.svg?inline'),
  usdt: require('cryptocurrency-icons/svg/color/usdt.svg?inline'),
  xrp: require('cryptocurrency-icons/svg/color/xrp.svg?inline'),
  generic: require('cryptocurrency-icons/svg/color/generic.svg?inline'),
}

export default {
  props: {
    name: {
      type: String,
      default: () => null,
      required: true,
      validator(value) {
        return Object.prototype.hasOwnProperty.call(cryptoIcons, value)
      },
    },
  },
  cryptoIconComponent(name) {
    return name ? cryptoIcons[name] : cryptoIcons.generic
  },
}
</script>
