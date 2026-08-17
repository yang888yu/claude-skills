# Claude Code Skills - 实测可用的5个

> 测试了一圈 Claude Code Skills，90%都是坑，只推荐这5个。

## ✅ 通过测试的 Skills

经过实际测试，以下5个 Skills **能顺利安装、真正好用**：

### 1. caveman - 省65% token
- **Star**: ~9.5万
- **功能**: Token 压缩，用极简措辞输出
- **效果**: 省约65%的 token
- **安装**: `curl -fsSL https://raw.githubusercontent.com/JuliusBrussee/caveman/main/install.sh | bash`
- **适合**: 所有人，跑长任务必备

### 2. graphify - 代码库知识图谱
- **Star**: ~10万
- **功能**: 把代码库转成可查询的知识图谱
- **效果**: AI 能看清代码结构、调用关系
- **安装**: 
  ```bash
  pip install graphifyy
  graphify install
  ```
- **适合**: 大项目（>1万行代码）

### 3. OpenSpec - 规格驱动开发
- **Star**: ~6.3万
- **功能**: 先写规格文档，再按规格实现
- **效果**: 让 AI 按约定编程，结果可验证
- **安装**: 
  ```bash
  npm install -g @fission-ai/openspec@latest
  cd your-project
  openspec init
  ```
- **适合**: 产品级开发

### 4. karpathy-skills - Karpathy 避坑清单
- **Star**: ~19.8万
- **功能**: Andrej Karpathy 总结的 LLM 编程陷阱规避规则
- **效果**: AI 主动避开常见坑（重复造轮子、过度抽象等）
- **安装**: 
  ```bash
  claude plugin marketplace add forrestchang/andrej-karpathy-skills
  claude plugin install andrej-karpathy-skills@karpathy-skills
  ```
- **适合**: 所有人，零成本高收益

### 5. claude-hud - 实时监控面板
- **Star**: ~2.7万
- **功能**: 可视化显示上下文用量、token 消耗
- **效果**: 知道 AI 在哪个环节、用了多少资源
- **安装**: 
  ```bash
  claude plugin marketplace add jarrodwatts/claude-hud
  claude plugin install claude-hud@claude-hud
  ```
- **适合**: 跑长任务、需要监控的场景

---

## 📊 测试标准

1. **10分钟能装好** - 依赖少、不报错
2. **文档清楚** - 看得懂怎么用
3. **真有效果** - 承诺的功能能实现
4. **会常用** - 不是装完就吃灰

---

## ❌ 没通过测试的

测试过程中还尝试了以下工具，但都有问题：

- **Context7** - 安装时卡住，交互式界面有bug
- **Playwright MCP** - 需要手动配置 MCP server，门槛高
- **Superpowers** - 依赖太多，安装报错
- **ECC** - 文档不清楚，看不懂怎么用
- **pua** - 名字敏感，实际效果不明显

---

## 🎯 推荐安装顺序

### 必装（2个）
1. **caveman** - 省 token，人人需要
2. **karpathy-skills** - 零成本避坑

### 按需选装（3个）
- 大项目 → **graphify**
- 正经开发 → **OpenSpec**
- 长任务 → **claude-hud**

**不要一次性全装**，用一段时间再加。

---

## 📝 相关文章

- [完整测评文章](./测试Claude-Skills.md)
- [发布指南](./发布指南-Claude-Skills.md)

---

## 🙏 致谢

感谢这些开源项目的作者：
- [JuliusBrussee/caveman](https://github.com/JuliusBrussee/caveman)
- [Graphify-Labs/graphify](https://github.com/Graphify-Labs/graphify)
- [Fission-AI/OpenSpec](https://github.com/Fission-AI/OpenSpec)
- [forrestchang/andrej-karpathy-skills](https://github.com/forrestchang/andrej-karpathy-skills)
- [jarrodwatts/claude-hud](https://github.com/jarrodwatts/claude-hud)

---

## 📄 License

MIT

---

**测试时间**: 2026-08-17  
**测试者**: 登哥  
**Claude Code 版本**: 2.1.232
