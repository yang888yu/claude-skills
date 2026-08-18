# Claude Code Skills - 实测可用的5个

> 亲测能装、真正好用的 Claude Code Skills 合集

## 🎯 包含的 Skills

### 1. caveman - 省65% token
- **功能**: Token 压缩工具
- **效果**: 用极简措辞，省约65%的 token
- **适合**: 所有人

### 2. karpathy-skills - Karpathy 避坑清单
- **功能**: Andrej Karpathy 总结的 LLM 编程陷阱规避规则
- **效果**: AI 主动避开常见坑
- **适合**: 所有人

### 3. claude-hud - 实时监控面板
- **功能**: 可视化显示上下文用量、token 消耗
- **效果**: 知道 AI 在干什么、用了多少资源
- **适合**: 跑长任务的人

### 4. graphify - 代码库知识图谱
- **功能**: 把代码库转成可查询的知识图谱
- **效果**: AI 能看清代码结构、调用关系
- **适合**: 大项目（>1万行代码）

### 5. OpenSpec - 规格驱动开发
- **功能**: 先写规格文档，再按规格实现
- **效果**: 让 AI 按约定编程，结果可验证
- **适合**: 产品级开发
- **注意**: OpenSpec 是 npm 包，需单独安装

---

## 🚀 快速安装

### 一键安装脚本（推荐）

```bash
# 克隆本仓库
git clone https://github.com/yang888yu/claude-skills.git
cd claude-skills

# 运行安装脚本
bash install.sh
```

安装脚本会自动：
- 复制 Skills 文件到 `~/.claude/skills/`
- 安装 OpenSpec（需要 Node.js）
- 安装 graphify（需要 Python）

### 手动安装

#### 1-3. caveman + karpathy-skills + claude-hud

```bash
# 复制到 Claude Code 的 skills 目录
cp -r skills/caveman ~/.claude/skills/
cp -r skills/karpathy-skills ~/.claude/skills/
cp -r skills/claude-hud ~/.claude/skills/
```

或者用 Claude Code 插件方式：
```bash
claude plugin marketplace add JuliusBrussee/caveman
claude plugin install caveman@caveman

claude plugin marketplace add forrestchang/andrej-karpathy-skills
claude plugin install andrej-karpathy-skills@karpathy-skills

claude plugin marketplace add jarrodwatts/claude-hud
claude plugin install claude-hud@claude-hud
```

#### 4. graphify

```bash
pip install graphifyy
graphify install
```

或直接复制：
```bash
cp -r skills/graphify ~/.claude/skills/
```

#### 5. OpenSpec

```bash
npm install -g @fission-ai/openspec@latest
```

---

## 📋 目录结构

```
skills/
├── caveman/           # Token 压缩工具
├── karpathy-skills/   # Karpathy 避坑清单
├── claude-hud/        # 实时监控面板
├── graphify/          # 代码库知识图谱
└── README.md          # 每个 Skill 的说明
```

---

## 🎓 使用方法

### caveman
装完后自动生效，AI 会用更简洁的方式输出。

### karpathy-skills
装完后自动生效，AI 会遵循避坑规则。

### claude-hud
装完后，运行 Claude Code 时会显示监控面板。

### graphify
在项目目录运行：
```bash
/graphify .
```

### OpenSpec
在项目目录运行：
```bash
openspec init
```

---

## ⚙️ 系统要求

- **Claude Code**: 2.1.232 或更高版本
- **Node.js**: 18+ (OpenSpec)
- **Python**: 3.8+ (graphify)
- **Git**: 用于克隆仓库

---

## 🧪 测试环境

- **操作系统**: Windows 11 Pro
- **Claude Code**: 2.1.232
- **测试日期**: 2026-08-17

---

## 📖 详细测评

完整测评文章：[测了一圈 Claude Skills，90%都是坑，只推荐这5个](https://mp.weixin.qq.com/s/xxx)

---

## 🙏 致谢

感谢这些开源项目的作者：
- [JuliusBrussee/caveman](https://github.com/JuliusBrussee/caveman)
- [forrestchang/andrej-karpathy-skills](https://github.com/forrestchang/andrej-karpathy-skills)
- [jarrodwatts/claude-hud](https://github.com/jarrodwatts/claude-hud)
- [Graphify-Labs/graphify](https://github.com/Graphify-Labs/graphify)
- [Fission-AI/OpenSpec](https://github.com/Fission-AI/OpenSpec)

---

## 📄 License

本仓库采用 MIT 协议开源。

各个 Skill 遵循其原项目的开源协议。

---

**测试者**: 登哥  
**更新时间**: 2026-08-17
