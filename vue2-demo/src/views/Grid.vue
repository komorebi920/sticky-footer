<template>
  <div class="root">
    <!-- div.content -->
    <div class="content">
      <!-- div.content-inside 的高度可以随意设置，亦可根据内容高度自适应 -->
      <div class="content-inside">Content 1</div>
      <div class="content-inside">Content 2</div>
      <div class="content-inside">Content 3</div>
    </div>
    <!-- div.footer 始终位于页面底部，无论页面内容高度能否填满页面 -->
    <div class="footer">Sticky Footer</div>
  </div>
</template>

<script>
export default {
  name: "Grid",
  data() {
    return {};
  },
  mounted() {
    console.log("Grid mounted");
  },
};
</script>

<style lang="scss" scoped>
.root {
  min-height: 100vh;
  text-align: center;
  display: grid;
  grid-template-rows: 1fr auto;

  .content-inside {
    height: 100px; /* .content-inside 的高度可以随意设置，亦可根据内容高度自适应 */
    line-height: 100px; /* 实现文字垂直居中 */
  }

  .footer {
    height: 50px; /* 这种方式可以不固定 .footer 的高度，这里只是为了撑开元素高度方便观察效果 */
    line-height: 50px; /* 实现文字垂直居中 */
    grid-row-start: 2;
    grid-row-end: 3;
  }
}
</style>
