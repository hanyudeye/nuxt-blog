<template>
  <!-- <Tutorial/> -->
  <div class="p-5">
    hello,world
    <el-button type="primary">Hello ELE</el-button>
    <!-- 链接 -->
    <NuxtLink to="/login">登录</NuxtLink>
    <el-link to="/login">链接</el-link>
    <Nav></Nav>
    <Footer />
  </div>

</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
