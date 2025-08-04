<template>
  <footer class="footer">
    <div class="footer-content">
      <p>© {{ currentYear }} cpolar + GitLab 演示项目 - 基于 Vue 3 构建</p>
      <p class="footer-note">演示通过cpolar内网穿透访问私有GitLab的完整工作流程</p>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      currentYear: new Date().getFullYear()
    }
  }
}
</script>

<style scoped>
.footer {
  background-color: #f8f9fa;
  border-top: 1px solid #e9ecef;
  padding: 25px 20px;
  margin-top: 10px;
  flex-shrink: 0;
  width: 100%;
}

.footer-content {
  max-width: 1200px;
  margin: 0 auto;
  text-align: center;
  padding: 0 10px;
}

.footer-content p {
  color: #666;
  margin-bottom: 8px;
  line-height: 1.5;
  word-wrap: break-word;
}

.footer-note {
  font-size: 0.9rem;
  color: #999;
  line-height: 1.4;
}

@media (max-width: 768px) {
  .footer {
    padding: 25px 15px;
    margin-top: 30px;
  }
  
  .footer-content {
    padding: 0 5px;
  }
  
  .footer-content p {
    font-size: 0.9rem;
  }
  
  .footer-note {
    font-size: 0.8rem;
  }
}
</style>