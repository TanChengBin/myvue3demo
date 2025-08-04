<template>
  <div class="header-container">
    <div class="logo">
      <h2>CPolar</h2>
    </div>
    <nav class="nav-links">
      <a href="#" class="nav-link">首页</a>
      <a href="#" class="nav-link">功能</a>
      <a href="#" class="nav-link">价格</a>
      <a href="#" class="nav-link">文档</a>
      <a href="#" class="nav-link">关于我们</a>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
.header-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 0;
  margin-bottom: 20px;
}

.logo h2 {
  color: var(--primary-color);
  margin: 0;
  font-size: 1.8rem;
  border: none;
}

.nav-links {
  display: flex;
  gap: 20px;
}

.nav-link {
  color: var(--text-color);
  font-weight: 500;
  padding: 5px 10px;
  border-radius: 4px;
  transition: all 0.3s ease;
}

.nav-link:hover {
  background-color: rgba(255, 140, 0, 0.2);
  color: var(--primary-color);
  text-decoration: none;
}

@media (max-width: 768px) {
  .header-container {
    flex-direction: column;
    gap: 15px;
  }
  
  .nav-links {
    width: 100%;
    justify-content: center;
    flex-wrap: wrap;
    gap: 10px;
  }
}
</style>