# GitHub 上传步骤指南

这个文件将指导你一步步把 cold-outreach-skill 上传到 GitHub。

## 准备工作

### 前置要求
- [ ] 有 GitHub 账号
- [ ] 安装了 Git（检查方法：在终端运行 `git --version`）
- [ ] 已经下载了这个文件夹到本地

### 如果没有安装 Git

**macOS**:
```bash
brew install git
```

**Windows**:
下载安装：https://git-scm.com/download/win

**Linux**:
```bash
sudo apt-get install git
```

---

## 步骤 1: 在 GitHub 上创建新仓库

1. 登录 GitHub.com
2. 点击右上角的 "+" → "New repository"
3. 填写信息：
   - **Repository name**: `cold-outreach-skill`
   - **Description**: "Professional networking and cold outreach skill for Claude AI"
   - **Public** (选中这个，让别人能看到)
   - **不要**勾选 "Initialize this repository with a README"（因为我们已经有了）
4. 点击 "Create repository"

---

## 步骤 2: 在本地初始化 Git

打开终端/命令行，进入 `cold-outreach-skill` 文件夹：

```bash
cd /path/to/cold-outreach-skill
```

初始化 Git 仓库：

```bash
git init
```

你应该看到：`Initialized empty Git repository in ...`

---

## 📦 步骤 3: 添加所有文件

```bash
git add .
```

这会把所有文件添加到 staging area。

检查状态：

```bash
git status
```

你应该看到所有文件都是绿色的 "new file"。

---

## 步骤 4: 创建第一次提交

```bash
git commit -m "Initial commit: Cold Outreach Skill for Claude"
```

---

## 步骤 5: 连接到 GitHub 仓库

**重要**：把下面的 `YOUR_USERNAME` 替换成你的 GitHub 用户名！

```bash
git remote add origin https://github.com/YOUR_USERNAME/cold-outreach-skill.git
```

检查是否连接成功：

```bash
git remote -v
```

你应该看到：
```
origin  https://github.com/YOUR_USERNAME/cold-outreach-skill.git (fetch)
origin  https://github.com/YOUR_USERNAME/cold-outreach-skill.git (push)
```

---

## 🚢 步骤 6: 推送到 GitHub

```bash
git branch -M main
git push -u origin main
```

第一次推送时，可能会要求你输入 GitHub 用户名和密码（或者 Personal Access Token）。

### 如果遇到密码问题

GitHub 不再支持密码登录，你需要创建 Personal Access Token：

1. 去 GitHub.com → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. 点击 "Generate new token (classic)"
3. 勾选 `repo` 权限
4. 复制生成的 token（只显示一次！）
5. 用这个 token 代替密码

---

## ✓ 步骤 7: 验证上传成功

1. 刷新你的 GitHub 仓库页面：`https://github.com/YOUR_USERNAME/cold-outreach-skill`
2. 你应该看到所有文件都已经上传
3. README.md 会自动显示在仓库首页

---

## 🎨 步骤 8: 完善仓库信息（可选）

### 添加 Topics

在仓库页面点击 "Add topics"，添加：
- `claude-ai`
- `cold-outreach`
- `networking`
- `job-search`
- `linkedin`
- `email-templates`

### 添加 Description

在仓库标题下方添加简短描述：
```
Professional networking and cold outreach skill for Claude AI - trained on real-world templates
```

### 启用 Issues

Settings → Features → 勾选 "Issues"

---

## 完整的文件结构

上传后，你的仓库应该有这个结构：

```
cold-outreach-skill/
├── README.md                     ← 项目首页
├── SKILL.md                      ← 核心 skill 文档
├── CONTRIBUTING.md               ← 贡献指南
├── EXAMPLES.md                   ← 使用示例
├── LICENSE                       ← MIT 许可证
├── .gitignore                    ← Git 忽略文件
└── references/
    ├── templates.md              ← 所有模板
    ├── coffee-chat-guide.md      ← Coffee chat 指南
    └── recruiter-strategy.md     ← Recruiter 策略
```

---

## 🔄 后续更新流程

当你需要更新内容时：

1. **修改文件**
2. **查看改动**:
   ```bash
   git status
   git diff
   ```

3. **添加改动**:
   ```bash
   git add .
   ```

4. **提交改动**:
   ```bash
   git commit -m "描述你的改动"
   ```

5. **推送到 GitHub**:
   ```bash
   git push
   ```

---

## 🐛 常见问题

### Q: `git push` 失败，提示 "Permission denied"

**A**: 你可能需要配置 Git 用户信息：

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### Q: 如何删除 GitHub 上的文件？

**A**: 
```bash
git rm filename
git commit -m "Remove filename"
git push
```

### Q: 如何修改已经 commit 的信息？

**A**: 
```bash
git commit --amend -m "New commit message"
git push --force
```

### Q: 如何撤销本地改动？

**A**:
```bash
git checkout -- filename  # 撤销单个文件
git reset --hard          # 撤销所有改动（危险！）
```

---

## 可选：使用 GitHub Desktop

如果你不习惯命令行，可以使用 GitHub Desktop：

1. 下载：https://desktop.github.com/
2. 安装并登录 GitHub 账号
3. File → Add Local Repository → 选择 cold-outreach-skill 文件夹
4. Publish repository
5. 以后的更新就可以用图形界面完成

---

## 完成！

恭喜！你的 cold-outreach-skill 现在已经在 GitHub 上了。

**下一步**：
1. 在 README 中添加你的 GitHub 用户名链接
2. 分享你的仓库链接
3. 邀请其他人 contribute

**仓库链接**：`https://github.com/YOUR_USERNAME/cold-outreach-skill`

---

## 提示

- 每次做改动后要记得 commit 和 push
- 写清楚的 commit message 方便以后查看
- 定期备份重要文件
- 可以用 GitHub Issues 来追踪改进想法
- 可以用 GitHub Projects 来管理开发计划

---

需要帮助？在仓库开一个 Issue 或者查看 GitHub 的官方文档：https://docs.github.com/
