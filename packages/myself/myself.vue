<template>
  <i :class="['v-icon', `v-icon-${name}`]" :style="getStyle" @click="handleClick">
    <slot />
  </i>
</template>

<script>
export default {
  name: 'v-myself',
  props: {
    name: {
      type: String,
      required: true
    },
    size: {
      type: [Number, String],
      default: 14
    },
    fontUnit: {
      type: String,
      validator (val) {
        return ['px', 'rem', 'em', '%', 'pt', 'pc', 'in', 'cm', 'mm', 'ex', 'vw', 'vh'].indexOf(val) > -1
      },
      default: 'px'
    },
    color: String
  },
  computed: {
    getStyle () {
      let style = {}
      this.size && (style.fontSize = this.size + this.fontUnit)
      this.color && (style.color = this.color)
      return style
    }
  },
  methods: {
    handleClick () {
      this.$emit('click')
    }
  }
}
</script>
