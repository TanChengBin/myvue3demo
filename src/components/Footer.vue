<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-section">
        <h3>关于CPolar</h3>
        <p>CPolar是一款专业的内网穿透工具，为开发者提供稳定、安全的内网映射服务。</p>
      </div>
      <div class="footer-section">
        <h3>快速链接</h3>
        <div class="quick-links">
          <a href="#">首页</a>
          <a href="#">功能介绍</a>
          <a href="#">价格</a>
          <a href="#">文档</a>
        </div>
      </div>
      <div class="footer-section">
        <h3>联系我们</h3>
        <p>邮箱：contact@cpolar.com</p>
        <p>技术支持：support@cpolar.com</p>
      </div>
    </div>
    <div class="footer-bottom">
      <p>© {{ currentYear }} CPolar 演示项目 - 基于Vue3和Vite构建</p>
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
  margin-top: auto;
  background-color: var(--card-bg);
  border-radius: var(--border-radius);
  padding: 20px;
  border-top: 1px solid #333;
}

.footer-content {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  gap: 30px;
  margin-bottom: 20px;
}

.footer-section {
  flex: 1;
  min-width: 200px;
}

.footer-section h3 {
  color: var(--primary-color);
  margin-bottom: 15px;
  font-size: 1.2rem;
}

.quick-links {
  display: flex;
  flex-wrap: wrap;
  gap: 15px;
}

.quick-links a {
  color: var(--text-color);
  text-decoration: none;
}

.quick-links a:hover {
  color: var(--primary-color);
}

.footer-bottom {
  text-align: center;
  padding-top: 15px;
  border-top: 1px solid #333;
  color: var(--light-text);
  font-size: 0.9rem;
}

@media (max-width: 768px) {
  .footer-content {
    flex-direction: column;
    gap: 20px;
  }
  
  .footer-section {
    width: 100%;
  }
}
</style>