<template>
  <div class="page-title">
    <h1>{{ title }}</h1>
    <p v-if="description">{{ description }}</p>
  </div>
</template>

<script>
export default {
  name: 'PageTitle',
  props: {
    description: {
      type: String,
      default: ''
    }
  },
  data() {
    return {
      title: this.$t(this.$route.meta.title)
    };
  }
};
</script>

<style lang="scss" scoped>
@import 'src/assets/styles/helpers';

.page-title {
  margin-bottom: $spacer * 2;
}
h1 {
  font-weight: $display4-weight;
  line-height: $display-line-height;
}
p {
  max-width: 72ch;
}
</style>
