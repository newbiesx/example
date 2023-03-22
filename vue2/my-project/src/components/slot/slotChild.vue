<template>
  <div class="container">
    <div>
        匿名插槽
        <slot></slot>
        <div>
          <slot name="content"></slot>
        </div>
        <h3>作用域插槽</h3>
        <span>
          <slot v-bind:user="user">
            {{ user.lastName }}
          </slot>
        </span>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  props: {},
  data() {
    return {
      user:{
        firstName:"诸葛",
        lastName:"亮"
      }
    };
  },
  watch: {},
  computed: {},
  methods: {},
  created() {},
  mounted() {}
};
</script>
<style scoped>
.container{}
</style>