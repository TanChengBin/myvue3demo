<template>
  <div class="app">
    <div class="content-wrapper">
      <Header />
      
      <main class="main-content">
        <section class="hero">
          <h1>cpolar + GitLab 演示项目</h1>
          <p class="subtitle">通过内网穿透访问私有GitLab仓库的完整演示</p>
          <div class="demo-badge">🚀 演示项目</div>
        </section>
        
        <section class="demo-info">
          <div class="info-grid">
            <div class="info-card">
              <h3>🔗 cpolar 内网穿透</h3>
              <p>将本地GitLab服务暴露到公网，实现远程访问</p>
            </div>
            <div class="info-card">
              <h3>📦 私有GitLab</h3>
              <p>搭建私有代码仓库，保护企业代码安全</p>
            </div>
            <div class="info-card">
              <h3>🔄 完整工作流</h3>
              <p>从代码提交到CI/CD部署的完整演示</p>
            </div>
          </div>
        </section>
        
        <section class="workflow-section">
          <h2>cpolar → GitLab 工作流程</h2>
          <div class="workflow-container">
            <div class="workflow-step">
              <div class="step-icon">🏠</div>
              <h4>本地GitLab</h4>
              <p>localhost:8888</p>
            </div>
            <div class="workflow-arrow">→</div>
            <div class="workflow-step">
              <div class="step-icon">🔗</div>
              <h4>cpolar隧道</h4>
              <p>内网穿透</p>
            </div>
            <div class="workflow-arrow">→</div>
            <div class="workflow-step">
              <div class="step-icon">🌐</div>
              <h4>公网访问</h4>
              <p>xxx.cpolar.top</p>
            </div>
            <div class="workflow-arrow">→</div>
            <div class="workflow-step">
              <div class="step-icon">👥</div>
              <h4>团队协作</h4>
              <p>远程开发</p>
            </div>
          </div>

        </section>
      </main>
    </div>
    
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Footer
  }
}
</script>

<style>
/* 全局样式重置 */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  line-height: 1.6;
  color: #333;
  background-color: #fff;
}

.app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.content-wrapper {
  flex: 1;
}

.main-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
  padding-bottom: 10px;
}

/* Hero 区域 */
.hero {
  text-align: center;
  padding: 30px 40px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  margin: 20px 0;
  border-radius: 12px;
  position: relative;
}

.hero h1 {
  font-size: 2rem;
  margin-bottom: 12px;
  font-weight: 600;
}

.subtitle {
  font-size: 1rem;
  opacity: 0.9;
  max-width: 500px;
  margin: 0 auto 15px;
}

.demo-badge {
  display: inline-block;
  background: rgba(255, 255, 255, 0.2);
  padding: 8px 16px;
  border-radius: 20px;
  font-size: 0.9rem;
  font-weight: 500;
  backdrop-filter: blur(10px);
}

/* 演示信息区域 */
.demo-info {
  padding: 25px 0;
}

.info-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 25px;
  margin-bottom: 30px;
}

.info-card {
  background: #fff;
  padding: 25px;
  border-radius: 10px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
  text-align: center;
  transition: all 0.3s ease;
  border: 2px solid transparent;
}

.info-card:hover {
  transform: translateY(-3px);
  border-color: #667eea;
  box-shadow: 0 8px 25px rgba(102, 126, 234, 0.15);
}

.info-card h3 {
  font-size: 1.3rem;
  color: #2c3e50;
  margin-bottom: 12px;
}

.info-card p {
  color: #666;
  line-height: 1.6;
  font-size: 0.95rem;
}

/* 工作流程区域 */
.workflow-section {
  padding: 20px 0;
  background-color: #f8f9fa;
  border-radius: 12px;
  margin: 15px 0;
}

.workflow-section h2 {
  text-align: center;
  font-size: 1.5rem;
  color: #2c3e50;
  margin-bottom: 15px;
  font-weight: 500;
}

.workflow-container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  gap: 15px;
  margin-bottom: 0;
  padding: 0 20px;
}

.workflow-step {
  text-align: center;
  min-width: 100px;
}

.step-icon {
  font-size: 2rem;
  margin-bottom: 8px;
}

.workflow-step h4 {
  color: #2c3e50;
  margin-bottom: 4px;
  font-size: 0.9rem;
}

.workflow-step p {
  color: #666;
  font-size: 0.8rem;
  margin: 0;
}

.workflow-arrow {
  font-size: 1.2rem;
  color: #667eea;
  font-weight: bold;
  margin: 0 8px;
}





.btn {
  background-color: #007bff;
  color: white;
  padding: 15px 30px;
  border: none;
  border-radius: 6px;
  font-size: 1.1rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
  margin-top: 20px;
}

.btn:hover {
  background-color: #0056b3;
}

/* 响应式设计 */
@media (max-width: 768px) {
  .hero h1 {
    font-size: 1.6rem;
  }
  
  .subtitle {
    font-size: 0.9rem;
  }
  
  .info-grid {
    grid-template-columns: 1fr;
    gap: 20px;
  }
  
  .main-content {
    padding: 0 15px;
  }
  
  .hero {
    padding: 25px 30px;
  }
  
  .workflow-section {
    padding: 20px 15px;
    margin: 15px 0;
  }
  
  .workflow-section h2 {
    font-size: 1.3rem;
  }
  
  .workflow-container {
    flex-direction: column;
    gap: 10px;
    padding: 0 10px;
  }
  
  .workflow-arrow {
    transform: rotate(90deg);
    margin: 3px 0;
  }
}
</style>