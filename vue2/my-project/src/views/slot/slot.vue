<template>
  <div class="container">
    <slot-child>
        <!-- <div>父组件匿名插槽内容</div> -->
        <template v-slot:content>
          父组件的具名插槽内容
        </template>
        <template v-slot="{user}">{{ user&&user.firstName }}</template>
    </slot-child>
  </div>
</template>

<script>
import slotChild from '../../components/slot/slotChild.vue';
export default {
  components: {slotChild},
  props: {},
  data() {
    return {
      user:null
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