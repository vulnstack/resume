# 小峰聊Ai · 在线简历（GitHub Pages）

深色安全运营终端风单页简历，零依赖、单文件，部署为 GitHub Pages 项目站点。

**最终访问地址：<https://vulnstack.github.io/resume/>**

> 为什么用独立 `resume` 仓库而不是 `vulnstack.github.io` 根仓库：
> 根仓库已承载现有个人主页（博客站点），简历放根目录会覆盖它；
> 项目站点方式两者并存、互不影响。

## 部署步骤（本目录下执行）

```bash
# 1. 在 github.com 用 vulnstack 账号新建一个 公开（Public）仓库，名字：resume
#    （不要勾选自动生成 README，保持空仓库）
# 2. 回到本目录执行：
git init
git config user.name  "vulnstack"
git config user.email "hongrisec2023@gmail.com"   # 仓库级配置，勿用公司邮箱
git add index.html README.md .nojekyll
git commit -m "resume: initial public version"
git branch -M main
git remote add origin https://github.com/vulnstack/resume.git
git push -u origin main
# 3. 打开 https://github.com/vulnstack/resume 的 Settings → Pages →
#    Source 选 main 分支 / 根目录（/(root)）→ Save
#    约 1 分钟后访问：https://vulnstack.github.io/resume/
```

推送时如要求登录：密码处填 Personal Access Token（GitHub → Settings →
Developer settings → Tokens (classic) → 勾选 repo 权限生成），不支持账号密码。

## 更新简历内容

改完 `index.html` 后只需：

```bash
git add index.html && git commit -m "update resume" && git push
```

## 内容安全基线（已脱敏项）

无真实姓名（展示名"小峰聊Ai"）、无雇主名称、无客户名称、无具体时间、
无电话/住址/出生信息、无教育背景；仅公开邮箱（hongrisec2023@gmail.com）
与 GitHub 入口；项目描述为成果级概述。首次推送前建议最后通读一遍
index.html 确认无新增敏感信息。
