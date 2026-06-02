# HITSZ Simulation Wiki

HITSZ Simulation Wiki 是课题组仿真知识库，用于沉淀 CFD、传热、多物理场建模、网格划分、Fluent/COMSOL 使用经验、UDF、后处理和问题排查方法。

当前阶段仅搭建网站框架、目录结构、导航、Netlify 部署配置和 GitHub 协作模板，具体技术内容将逐步补充。

## 本地运行

首次拉取仓库后安装依赖：

```bash
npm install
```

启动本地开发服务器：

```bash
npm run docs:dev
```

## 构建方法

生成静态站点：

```bash
npm run docs:build
```

本地预览构建结果：

```bash
npm run docs:preview
```

## Netlify 部署设置

Netlify 使用仓库根目录下的 `netlify.toml` 自动构建：

- Build command: `npm run docs:build`
- Publish directory: `docs/.vitepress/dist`
- Node.js version: `20`

## 投稿方式

- 仿真问题请使用 GitHub Issues 中的“提交仿真问题”表单。
- 已解决问题建议整理为“提交已解决案例”。
- 正式文档修改请通过 Pull Request 提交。
- PR 中请说明修改页面、修改原因、是否本地运行过 `npm run docs:build`，以及是否关联 Issue。

请勿上传涉密项目数据、企业合作图纸、账号密码、未公开论文数据或大型仿真文件。

## 仓库目录说明

```text
docs/                         VitePress 文档源码
docs/.vitepress/config.mts    VitePress 站点配置
docs/simulation-basics/       仿真通识
docs/ansys/                   Ansys 生态
docs/comsol/                  COMSOL 生态
docs/cases/                   项目案例
docs/troubleshooting/         问题排查
docs/contributing.md          投稿指南
.github/ISSUE_TEMPLATE/       GitHub Issue Forms
.github/PULL_REQUEST_TEMPLATE.md
netlify.toml                  Netlify 部署配置
```

