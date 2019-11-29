<template lang="pug">
  div
    span.fa-stack.fa-1x.fa-fw
      i.far.fa-circle.fa-stack-2x.circle.fa-fw
      i.fa-stack-1x.this-fa.fa-fw.fa-inverse.nav-icon( :class="faClass")
</template>

<script>
export default {
  name: "IconStack",
  props: ["faClass"]
};
</script>
