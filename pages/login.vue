<template>
  <div class="min-h-screen flex justify-center items-center bg-gray-100">
    <el-card class="w-full sm:w-96 p-6 shadow-md rounded-lg">
      <h2 class="text-2xl font-semibold text-center mb-6">登录</h2>

      <el-form :model="form" ref="form" label-width="100px" class="space-y-4">
        <el-form-item label="邮箱" :rules="[{ required: true, message: '请输入邮箱', trigger: 'blur' }, { type: 'email', message: '请输入有效的邮箱地址', trigger: 'blur' }]">
          <el-input v-model="form.email" placeholder="请输入邮箱"></el-input>
        </el-form-item>

        <el-form-item label="密码" :rules="[{ required: true, message: '请输入密码', trigger: 'blur' }]">
          <el-input type="password" v-model="form.password" placeholder="请输入密码"></el-input>
        </el-form-item>

        <el-form-item>
          <el-button type="primary" @click="submitForm" class="w-full">登录</el-button>
        </el-form-item>
      </el-form>
    </el-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        email: '',
        password: ''
      }
    }
  },
  methods: {
    submitForm() {
      this.$refs.form.validate(valid => {
        if (valid) {
          // 处理登录逻辑
          console.log('表单有效', this.form)
          // 例如，调用登录 API
        } else {
          console.log('表单无效');
          return false;
        }
      });
    }
  }
}
</script>

<style scoped>
/* 页面居中样式 */
.el-card {
  background-color: white;
}
</style>
