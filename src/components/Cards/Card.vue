<template>
  <div class="card">    
    <div class="card-header" v-if="$slots.header || title">
      <slot name="header">
        <h4 class="card-title">{{title}}</h4>
        <p class="card-category" v-if="subTitle">{{subTitle}}</p>
      </slot>
    </div>
    <div class="card-body" v-if="$slots.default">
      <slot></slot>
    </div>
    <slot name="raw-content"></slot>
    
  </div>
</template>
<script>
export default {
  name: "card",
  props: {
    title: String,
    subTitle: String
  }
};
</script>
<style>
</style>
