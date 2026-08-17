# 《测了一圈 Claude Skills，90%都是坑，只推荐这5个》- 发布指南

## ✅ 已完成的工作

### 1. 测试完成（5个 Skills）
- ✅ **caveman** - 省65% token（9.5万 stars）
- ✅ **graphify** - 代码知识图谱（10万 stars）
- ✅ **OpenSpec** - 规格驱动开发（6.3万 stars）
- ✅ **karpathy-skills** - Karpathy避坑清单（19.8万 stars）
- ✅ **claude-hud** - 实时监控面板（2.7万 stars）

### 2. 文章撰写
- **标题**：《测了一圈 Claude Skills，90%都是坑，只推荐这5个》
- **篇幅**：约3000字
- **结构**：开头（为什么测）+ 测试标准 + 5个工具详解 + 失败的简述 + 选择建议
- **文件位置**：`D:\学习\公众号\草稿\测试Claude-Skills.md`

### 3. HTML格式转换
- **已生成**：`D:\学习\公众号\草稿\测试Claude-Skills.html`
- **已复制到剪贴板**：可直接粘贴到微信公众号编辑器

### 4. 配图生成
- **封面图**（2.35:1）：已生成
- **5张配图**：全部生成完成
- **位置**：`D:\学习\公众号\草稿\images\`

---

## 📁 文件清单

```
D:\学习\公众号\草稿\
├── 测试Claude-Skills.md          # 原始 Markdown
├── 测试Claude-Skills.html        # 微信格式 HTML ⭐
└── images/
    ├── article_01_130733.png    # 配图1 - caveman
    ├── article_02_130933.png    # 配图2 - graphify
    ├── article_03_131021.png    # 配图3 - OpenSpec
    ├── article_04_131105.png    # 配图4 - karpathy-skills
    └── article_05_131220.png    # 配图5 - claude-hud
```

---

## 🚀 发布步骤

### 方案A：手动发布（推荐）

1. **打开微信公众号后台** → 新建图文

2. **粘贴HTML**
   - HTML已在剪贴板
   - 直接 Ctrl+V 粘贴到编辑器
   - 格式会自动保留

3. **插入配图**
   - 在对应位置插入图片：
     - "### 1. caveman" 下方 → `article_01_130733.png`
     - "### 2. graphify" 下方 → `article_02_130933.png`
     - "### 3. OpenSpec" 下方 → `article_03_131021.png`
     - "### 4. karpathy-skills" 下方 → `article_04_131105.png`
     - "### 5. claude-hud" 下方 → `article_05_131220.png`

4. **上传封面图**
   - 位置：`D:\学习\AI产品开发\生图工具\output\2026-08-17\`
   - 找最新的 `cover_wechat_*.png`

5. **填写摘要**（建议）
   ```
   测了一圈 Claude Skills，90%装不上或没用。3天筛出这5个真能用的，帮你避坑。
   ```

6. **保存草稿**

---

### 方案B：自动发布（需配置）

如果配置了微信 API（`WECHAT_APP_ID` + `WECHAT_APP_SECRET`），可以一键发布：

```bash
cd "D:\学习\AI产品开发\公众号工具"
node index.js "D:\学习\公众号\草稿\测试Claude-Skills.md" \
  -t simple \
  --publish wechat \
  --draft-only \
  --publish-author "登哥"
```

---

## 📊 文章数据

- **字数**：约3000字
- **图片**：6张（1封面 + 5配图）
- **工具数量**：5个通过测试 + 5个失败案例
- **预计阅读时间**：6-8分钟

---

## 💡 优化建议

### 标题可以A/B测试
- 当前：《测了一圈 Claude Skills，90%都是坑，只推荐这5个》
- 备选1：《我花3天测试了12个 Claude Skills，只有这5个能用》
- 备选2：《别乱装！测了一圈 Claude Skills，90%都是坑》

### 可以加的互动
- 开头加：你装过哪些 Claude Skills？踩过什么坑？
- 结尾加：你最想要哪个功能的 Skill？评论区告诉我

### SEO优化
- 标题包含关键词：Claude Skills、测试、推荐
- 文中多次出现：Claude Code、Skills、插件、工具
- 适合搜索场景："Claude Code 插件推荐"、"Claude Skills 哪个好用"

---

## ⚠️ 注意事项

1. **配图插入位置很重要**：要插在对应工具的介绍下方，不要乱插
2. **HTML格式**：如果粘贴后格式乱了，可以用"清除格式"再重新粘贴
3. **封面图比例**：2.35:1 是微信推荐比例，不要裁剪
4. **链接检查**：文中没有外部链接，符合微信规范

---

**生成时间**：2026-08-17 13:12  
**工具**：Claude Code + 公众号工具 + 生图工具  
**总耗时**：约2小时（测试1.5h + 写作30min）
