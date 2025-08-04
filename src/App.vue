<template>
  <div class="container">
    <Header />
    <header class="banner">
      <h1><span class="highlight">CPolar</span> 内网穿透工具 <span class="demo-tag">演示项目</span></h1>
    </header>
    
    <div class="content-grid">
      <!-- 左侧栏 -->
      <div class="left-column">
        <section class="intro">
          <h2>什么是<span class="highlight">CPolar</span>？</h2>
          <p>CPolar是一款功能强大的内网穿透工具，帮助开发者轻松实现将本地服务器暴露到公网。</p>
        </section>
        
        <section class="use-cases">
          <h2>应用场景</h2>
          <div class="case-item">
            <h3><span class="highlight">●</span> 本地开发测试</h3>
            <p>将本地环境暴露到公网，方便团队成员远程访问。</p>
          </div>
          <div class="case-item">
            <h3><span class="highlight">●</span> 微信开发</h3>
            <p>配置外网可访问的回调地址。</p>
          </div>
        </section>
      </div>
      
      <!-- 中间栏 -->
      <div class="center-column">
        <section class="features">
          <h2>主要特点</h2>
          <ul>
            <li>
              <strong><span class="highlight">快速部署</span></strong> - 几分钟内完成配置
            </li>
            <li>
              <strong><span class="highlight">安全可靠</span></strong> - 加密通信，保障数据安全
            </li>
            <li>
              <strong><span class="highlight">多平台支持</span></strong> - Windows、macOS、Linux
            </li>
            <li>
              <strong><span class="highlight">自定义域名</span></strong> - 提升专业形象
            </li>
          </ul>
        </section>
      </div>
      
      <!-- 右侧栏 -->
      <div class="right-column">
        <section class="quick-start">
          <h2>快速开始</h2>
          <div class="code-block">
            <code>
              # 安装CPolar<br>
              npm install cpolar -g<br><br>
              # 启动服务<br>
              cpolar http 8080
            </code>
          </div>
          <button class="btn">立即下载</button>
        </section>
        
        <section class="testimonial">
          <h2>用户评价</h2>
          <div class="quote">
            <p>"CPolar让我的开发工作变得更加高效，强烈推荐！"</p>
            <div class="author">— 某资深开发者</div>
          </div>
        </section>
      </div>
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
/* 全局样式 */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'PingFang SC', 'Microsoft YaHei', sans-serif;
  line-height: 1.6;
  color: var(--text-color);
  background-color: var(--background);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 10px;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.banner {
  text-align: center;
  padding: 10px 0;
  background-color: var(--card-bg);
  color: var(--text-color);
  border-radius: var(--border-radius);
  margin-bottom: 15px;
  border-bottom: 2px solid var(--primary-color);
}

.highlight {
  color: var(--primary-color);
  font-weight: bold;
}

.demo-tag {
  background-color: var(--primary-color);
  color: #000;
  font-size: 0.9rem;
  padding: 3px 8px;
  border-radius: 4px;
  margin-left: 10px;
  vertical-align: middle;
}

h1 {
  font-size: 2rem;
}

h2 {
  color: var(--text-color);
  margin: 15px 0;
  padding-bottom: 8px;
  border-bottom: 1px solid #333;
  font-size: 1.3rem;
}

h3 {
  font-size: 1.1rem;
  margin-bottom: 8px;
}

/* 网格布局 */
.content-grid {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 10px;
  margin-bottom: 15px;
  height: auto;
  max-height: 450px;
}

.left-column, .center-column, .right-column {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

section {
  background: var(--card-bg);
  padding: 15px;
  border-radius: var(--border-radius);
  box-shadow: var(--box-shadow);
  height: 100%;
}

/* 特性列表 */
.features ul {
  list-style-type: none;
}

.features li {
  margin: 12px 0;
  padding-left: 20px;
  position: relative;
}

.features li:before {
  content: "✓";
  color: var(--primary-color);
  position: absolute;
  left: 0;
}

/* 应用场景 */
.use-cases .case-item {
  margin-bottom: 15px;
}

/* 代码块 */
.code-block {
  background-color: #2a2a2a;
  border-radius: var(--border-radius);
  padding: 15px;
  margin: 15px 0;
  font-family: monospace;
  white-space: pre-wrap;
}

/* 按钮 */
.btn {
  display: inline-block;
  background-color: var(--primary-color);
  color: #000;
  font-weight: bold;
  padding: 8px 20px;
  border-radius: var(--border-radius);
  border: none;
  cursor: pointer;
  transition: background-color 0.3s;
  margin-top: 10px;
}

.btn:hover {
  background-color: var(--secondary-color);
}

/* 用户评价 */
.quote {
  font-style: italic;
  border-left: 3px solid var(--primary-color);
  padding-left: 10px;
  margin: 10px 0;
}

.author {
  text-align: right;
  color: var(--light-text);
  margin-top: 5px;
}

/* 响应式设计 */
@media (max-width: 768px) {
  .content-grid {
    grid-template-columns: 1fr;
    height: auto;
  }
  
  section {
    margin-bottom: 15px;
  }
}
</style>