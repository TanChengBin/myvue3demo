# cpolar + GitLab 演示项目

> **项目说明**: 这是一个使用Vue3和Vite构建的cpolar内网穿透与GitLab集成演示项目。  
> **cpolar官网**: https://cpolar.com  
> **GitLab官网**: https://gitlab.com

这是一个演示如何使用cpolar内网穿透工具将本地GitLab服务暴露到公网的完整项目，实现团队远程协作开发的解决方案。

## 项目特点

- 基于Vue3框架
- 使用Vite构建工具
- 简洁的UI设计
- 响应式布局
- 演示cpolar内网穿透功能
- 展示GitLab私有仓库远程访问
- 完整的工作流程演示

## 快速开始

```bash
# 安装依赖
npm install

# 启动开发服务器
npm run dev

# 构建生产版本
npm run build

# 预览生产版本
npm run preview
```

## 项目结构

```
myvue3demo/
├── public/         # 静态资源
├── src/            # 源代码
│   ├── assets/     # 资源文件
│   ├── components/ # 组件
│   ├── App.vue     # 主应用组件
│   └── main.js     # 入口文件
├── index.html      # HTML模板
├── vite.config.js  # Vite配置
└── package.json    # 项目配置
```

## 核心功能演示

本项目演示了以下核心功能：

- **内网穿透**: 使用cpolar将本地GitLab暴露到公网
- **私有仓库**: 搭建和管理私有GitLab代码仓库
- **远程访问**: 通过公网域名访问本地GitLab服务
- **团队协作**: 支持多人远程协作开发
- **完整工作流**: 从本地部署到公网访问的完整流程
- **安全访问**: 保护企业代码安全的同时实现远程访问

## 技术栈

- **前端框架**: Vue 3
- **构建工具**: Vite
- **内网穿透**: cpolar
- **代码托管**: GitLab (私有部署)
- **版本控制**: Git
- **包管理**: npm

## cpolar + GitLab 工作流程

1. **本地GitLab部署**: 在本地服务器部署GitLab (localhost:8888)
2. **cpolar隧道建立**: 使用cpolar创建内网穿透隧道
3. **公网域名映射**: 获得公网访问域名 (xxx.cpolar.top)
4. **团队远程访问**: 团队成员通过公网域名访问私有GitLab
5. **协作开发**: 实现代码提交、分支管理、合并请求等完整工作流

## 演示内容

本项目的Web界面展示了：
- cpolar内网穿透的工作原理
- GitLab私有仓库的优势
- 完整的工作流程图
- 技术栈介绍
- 实际应用场景

## 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。