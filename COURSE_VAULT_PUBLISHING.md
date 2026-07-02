# 课程知识库 Quartz 发布说明

## 当前结构

- Quartz 项目：`/Users/johnwong/Documents/Codex/quartz-course-site`
- Obsidian 库：`/Users/johnwong/Library/CloudStorage/坚果云-junxw1102@163.com/Work Documents/Obsidian Hub/课程知识库`
- Quartz `content`：symlink 指向上述 Obsidian 库
- Quartz `content-publish`：本地发布镜像，用于避免坚果云 CloudStorage 读取超时
- 配置文件：`quartz.config.yaml`

这种结构不会复制或移动 Obsidian 文件。日常发布建议先生成 `content-publish` 本地镜像，再让 Quartz 读取镜像。

## 当前状态

项目已完成：

1. 克隆 Quartz 5。
2. 安装主项目 npm 依赖，使用项目本地 cache：`.npm-cache`。
3. 初始化为 Obsidian 模板。
4. 将 `content` 链接到 Obsidian 课程知识库。
5. 配置中文站点标题、中文 locale、GitHub Pages baseUrl。
6. 忽略 `.obsidian`、`.DS_Store`、`图谱视图`、`_系统`。
7. 已安装 Quartz 5 社区插件。
8. 已生成 `.quartz/plugins/index.ts` 插件入口。
9. 已生成 `content-publish` 本地发布镜像。
10. 已成功构建并启动本地预览。

当前本地预览：

```text
http://localhost:8080
```

当前临时未发布：

- `交通工程`：已部分发布；坚果云 CloudStorage 中读取超时的文件暂未进入镜像。
- `申请材料-面试知识库`：含申请与面试材料，默认不公开。

已发布分区：

- `数学建模与优化`
- `工程基础与跨学科`
- `计算机与数据分析`
- `能源管理与环境`
- `铁路安全与控制系统`
- `风险可靠性`
- `交通工程`（部分）

## 本地预览命令

在项目目录执行：

```bash
cd /Users/johnwong/Documents/Codex/quartz-course-site
python3 /Users/johnwong/Documents/Codex/2026-06-28/wo-x/make_quartz_publish_mirror.py
node quartz/bootstrap-cli.mjs build --serve --port 8080 --directory content-publish
```

如果重新克隆项目或 `.quartz/` 插件目录不存在，需要先安装插件：

```bash
npm run install-plugins
```

注意：Quartz 5 官方要求 Node 22。当前本机 `/opt/homebrew/bin/node` 是 Node 25，官方 `npm run install-plugins` 可能因为 `.scss` loader 兼容问题失败；GitHub Actions 或本地 Node 22 环境应正常。

## GitHub Pages 发布

当前 `baseUrl` 是：

```yaml
baseUrl: johnwong.github.io/course-vault
```

如果实际仓库名不是 `course-vault`，需要把 `quartz.config.yaml` 里的 `baseUrl` 改成：

```yaml
baseUrl: <GitHub用户名>.github.io/<仓库名>
```

然后按 Quartz 官方 hosting 流程配置 GitHub Pages / GitHub Actions。

## 内容同步策略

不要移动 Obsidian 库。后续新增课程只需要写入原 Obsidian 库，再重新运行：

```bash
python3 /Users/johnwong/Documents/Codex/2026-06-28/wo-x/make_quartz_publish_mirror.py
node quartz/bootstrap-cli.mjs build --directory content-publish
```

Quartz 会从 `content-publish` 本地镜像读取最新内容。镜像报告在：

```text
/Users/johnwong/Documents/Codex/quartz-course-site/content-publish-report.json
```

## 交通工程完整发布

当前 `交通工程` 已可部分发布，但仍有若干坚果云文件读取超时。要完整发布有两条路：

1. 在坚果云客户端里把 `课程知识库/交通工程` 设为离线可用，然后重新生成镜像。
2. 继续使用镜像脚本，等待后续同步完成；脚本会把新变得可读的文件补进 `content-publish`。
