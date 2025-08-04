<template>
  <header class="header">
    <div class="header-content">
      <div class="logo">
        <h2>cpolar + GitLab 演示</h2>
      </div>
      <nav class="nav">
        <a href="#" class="nav-link" @click.prevent="showDemo">演示说明</a>
        <a href="#" class="nav-link" @click.prevent="showTech">技术栈</a>
        <a href="#" class="nav-link" @click.prevent="showSource">源码</a>
      </nav>
    </div>
    
    <!-- 弹窗 -->
    <div v-if="showModal" class="modal-overlay" @click="closeModal">
      <div class="modal-content" @click.stop>
        <div class="modal-header">
          <h3>{{ modalTitle }}</h3>
          <button class="close-btn" @click="closeModal">×</button>
        </div>
        <div class="modal-body" v-html="modalContent"></div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      showModal: false,
      modalTitle: '',
      modalContent: ''
    }
  },
  methods: {
    showDemo() {
      this.modalTitle = '演示说明'
      this.modalContent = `
        <div class="demo-content">
          <h4>🎯 项目目标</h4>
          <p>本项目演示如何使用cpolar内网穿透工具，将本地搭建的GitLab服务暴露到公网，实现团队远程协作开发。</p>
          
          <h4>🔧 演示环境</h4>
          <ul>
            <li><strong>本地GitLab</strong>: 运行在localhost:8888</li>
            <li><strong>cpolar隧道</strong>: 提供内网穿透服务</li>
            <li><strong>公网域名</strong>: xxx.cpolar.top</li>
          </ul>
          
          <h4>👥 适用场景</h4>
          <ul>
            <li>企业内部代码管理</li>
            <li>远程团队协作开发</li>
            <li>临时项目演示</li>
            <li>开发环境快速分享</li>
          </ul>
          
          <h4>⚠️ 注意事项</h4>
          <p>这是一个技术演示项目，生产环境使用时请注意安全配置和访问控制。</p>
        </div>
      `
      this.showModal = true
    },
    
    showTech() {
      this.modalTitle = '技术栈'
      this.modalContent = `
        <div class="tech-content">
          <h4>🎨 前端技术</h4>
          <ul>
            <li><strong>Vue 3</strong> - 渐进式JavaScript框架</li>
            <li><strong>Vite</strong> - 快速的前端构建工具</li>
            <li><strong>CSS3</strong> - 现代样式设计</li>
            <li><strong>JavaScript ES6+</strong> - 现代JavaScript语法</li>
          </ul>
          
          <h4>🔧 核心工具</h4>
          <ul>
            <li><strong>cpolar</strong> - 内网穿透工具</li>
            <li><strong>GitLab</strong> - 代码管理平台</li>
            <li><strong>Git</strong> - 版本控制系统</li>
            <li><strong>Docker</strong> - 容器化部署(可选)</li>
          </ul>
          
          <h4>📦 项目结构</h4>
          <ul>
            <li><strong>src/components/</strong> - Vue组件</li>
            <li><strong>src/assets/</strong> - 静态资源</li>
            <li><strong>public/</strong> - 公共文件</li>
            <li><strong>package.json</strong> - 项目配置</li>
          </ul>
          
          <h4>🚀 构建部署</h4>
          <ul>
            <li><strong>开发环境</strong>: npm run dev</li>
            <li><strong>生产构建</strong>: npm run build</li>
            <li><strong>预览</strong>: npm run preview</li>
          </ul>
        </div>
      `
      this.showModal = true
    },
    
    showSource() {
      this.modalTitle = '源码信息'
      this.modalContent = `
        <div class="source-content">
          <h4>📂 项目源码</h4>
          <p>本项目源码托管在GitHub，欢迎查看和贡献代码。</p>
          
          <div class="source-links">
            <a href="https://github.com/TanChengBin/myvue3demo" target="_blank" class="source-link">
              🔗 GitHub仓库
            </a>
          </div>
          
          <h4>📋 快速开始</h4>
          <div class="code-block">
            <pre><code># 克隆项目
git clone https://github.com/TanChengBin/myvue3demo.git

# 安装依赖
cd myvue3demo
npm install

# 启动开发服务器
npm run dev</code></pre>
          </div>
          
          <h4>📄 许可证</h4>
          <p>本项目采用 <strong>MIT License</strong> 开源许可证。</p>
          
          <h4>🤝 贡献指南</h4>
          <ul>
            <li>Fork 项目到你的GitHub</li>
            <li>创建功能分支</li>
            <li>提交你的修改</li>
            <li>发起 Pull Request</li>
          </ul>
          
          <h4>📧 联系方式</h4>
          <p>如有问题或建议，欢迎通过GitHub Issues联系。</p>
        </div>
      `
      this.showModal = true
    },
    
    closeModal() {
      this.showModal = false
    }
  }
}
</script>

<style scoped>
.header {
  background-color: #fff;
  border-bottom: 1px solid #e9ecef;
  padding: 0 20px;
}

.header-content {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 0;
}

.logo h2 {
  color: #2c3e50;
  font-size: 1.8rem;
  font-weight: 400;
}

.nav {
  display: flex;
  gap: 30px;
}

.nav-link {
  color: #666;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.3s ease;
}

.nav-link:hover {
  color: #007bff;
}

/* 弹窗样式 */
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.modal-content {
  background: white;
  border-radius: 12px;
  max-width: 600px;
  max-height: 80vh;
  width: 90%;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
}

.modal-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  border-bottom: 1px solid #e9ecef;
  background-color: #f8f9fa;
}

.modal-header h3 {
  margin: 0;
  color: #2c3e50;
  font-size: 1.3rem;
}

.close-btn {
  background: none;
  border: none;
  font-size: 1.5rem;
  cursor: pointer;
  color: #666;
  padding: 0;
  width: 30px;
  height: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  transition: background-color 0.3s;
}

.close-btn:hover {
  background-color: #e9ecef;
}

.modal-body {
  padding: 20px;
  max-height: 60vh;
  overflow-y: auto;
}

.modal-body h4 {
  color: #2c3e50;
  margin: 20px 0 10px 0;
  font-size: 1.1rem;
}

.modal-body h4:first-child {
  margin-top: 0;
}

.modal-body p {
  color: #666;
  line-height: 1.6;
  margin-bottom: 15px;
}

.modal-body ul {
  color: #666;
  line-height: 1.6;
  margin-bottom: 15px;
  padding-left: 20px;
}

.modal-body li {
  margin-bottom: 5px;
}

.source-links {
  margin: 15px 0;
}

.source-link {
  display: inline-block;
  background-color: #007bff;
  color: white;
  padding: 10px 20px;
  border-radius: 6px;
  text-decoration: none;
  transition: background-color 0.3s;
}

.source-link:hover {
  background-color: #0056b3;
  color: white;
}

.code-block {
  background-color: #f8f9fa;
  border-radius: 6px;
  padding: 15px;
  margin: 15px 0;
  border-left: 4px solid #007bff;
}

.code-block pre {
  margin: 0;
  font-family: 'Monaco', 'Menlo', 'Ubuntu Mono', monospace;
  font-size: 0.9rem;
  line-height: 1.4;
  color: #333;
}

@media (max-width: 768px) {
  .header-content {
    flex-direction: column;
    gap: 20px;
  }
  
  .nav {
    gap: 20px;
  }
  
  .modal-content {
    width: 95%;
    max-height: 90vh;
  }
  
  .modal-header {
    padding: 15px;
  }
  
  .modal-body {
    padding: 15px;
  }
}
</style>