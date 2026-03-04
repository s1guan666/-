# 牢大打字 — 🚀 **单文件离线打字练习器**

![GitHub stars](https://img.shields.io/github/stars/your-repo/牢大打字?style=social) ![GitHub forks](https://img.shields.io/github/forks/your-repo/牢大打字?style=social) ![GitHub last commit](https://img.shields.io/github/last-commit/your-repo/牢大打字)

> **Last updated:** 2026-03-04

---

🎯 **项目概述**

- 🖥️ **单文件实现**：核心代码集中于 `App/app.html`，无需额外依赖。
- 🎵 **多主题音效**：支持 `牢大`、`坤坤`、`自定义` 音效主题。
- 🌐 **兼容性优先**：适配老旧浏览器，避免现代 API 引发的白屏问题。
- 📊 **大规模题库**：动态生成 50k 中文词、50k 英文词、5k 中文句子。
- 🔄 **负反馈机制**：确保生成内容质量，避免重复与低质量题目。

---

## 🌟 **主要功能**

| 功能                | 描述                                                                 |
|---------------------|----------------------------------------------------------------------|
| 🎵 **音频主题**      | `牢大`、`坤坤`、`自定义`，支持上传本地音频并持久化到浏览器存储。         |
| ✍️ **英文模式**      | 按单词输入，空格确认，避免单字符误判。                                 |
| 📚 **题库支持**      | 动态生成大规模题库，启动速度快，覆盖广。                               |
| 🔄 **质量控制**      | 验证生成内容，失败重试，回退模板，避免重复。                           |
| 🌐 **兼容性**        | 避免使用 async/await 等现代 API，确保老旧浏览器运行流畅。               |

---

## 📂 **代码结构**

```plaintext
📦 牢大打字
├── App/
│   ├── app.html          # 核心单文件应用
│   ├── 坤坤音频/          # 坤坤模式音频与图片资源
│   ├── 牢大音频/          # 牢大模式音频与图片资源
├── scripts/
│   ├── watch_update_readme.js  # 自动更新时间脚本
├── run_update_readme.bat  # Windows 启动脚本
└── README.md              # 项目说明文件
```

---

## 🚀 **快速开始**

1. **直接运行**：
   - 打开 `App/app.html` 即可在浏览器中运行。
   - 或运行打包的 exe 文件（如 `牢大打字.exe`）。

2. **主要交互说明**：
   - 🎵 **选择音频主题**：点击 `牢大` / `坤坤` / `自定义` 按钮切换。
   - 📂 **上传自定义音频**：点击“上传”按钮，选择音频文件。
   - ✍️ **英文模式**：输入单词后按空格确认。

---

## 🛠️ **开发者指南**

### 自动更新 README

1. **运行 Watcher**：

```bash
node scripts/watch_update_readme.js
```

2. **Git 提交钩子**：

在 `.git/hooks/pre-commit` 中添加：

```bash
node scripts/watch_update_readme.js --once
```

3. **CI 集成**：

在 CI 流程中运行：

```bash
node scripts/watch_update_readme.js --once
```

---

## 🐞 **常见问题**

- **白屏问题**：
  - 检查是否使用了 async/await 等现代 API。
  - 替换为兼容实现（如 FileReader 回调）。

- **自定义音频无法保存**：
  - 确认浏览器是否允许 localStorage。

- **英文模式单词确认失败**：
  - 确保按下空格键确认单词。

---

## 🤝 **贡献**

欢迎提交 Issue 或 PR！

- **改进生成策略**：
  - 导入更自然的语料库。
  - 增加严格质量控制。

- **扩展功能**：
  - 自动生成 CHANGELOG。
  - 集成更多音效主题。

---

> **Made with ❤️ by 牢大打字团队**

---

## 📷 项目预览

![App Screenshot](./屏幕截图%202026-03-04%20131958.png)

---

## 📤 快速上传到 GitHub

请在根目录 `E:\牢大打字` 执行以下命令：

```powershell
# 1. 添加所有文件
git add .

# 2. 提交更改
git commit -m "init"

# 3. 关联你的远程仓库
git remote add origin https://github.com/s1guan666/-.git

# 4. 推送到 GitHub
git branch -M main
git push -u origin main
```


---

## 📷 项目预览

![App Screenshot](./屏幕截图%202026-03-04%20131958.png)

---

## 📤 快速上传到 GitHub

请在根目录 `E:\牢大打字` 执行以下命令：

```powershell
# 1. 添加所有文件
git add .

# 2. 提交更改
git commit -m "feat: 初始提交，包含应用和说明文档"

# 3. 关联你的远程仓库 (请替换下面的 URL)
git remote add origin https://github.com/你的用户名/你的仓库名.git

# 4. 推送到 GitHub
git branch -M main
git push -u origin main
```

