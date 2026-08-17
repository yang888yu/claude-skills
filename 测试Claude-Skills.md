# 测了一圈 Claude Skills，90%都是坑，只推荐这5个

我最近测试了一圈 Claude Code Skills，想找几个真正提效的。

结果很残酷：大部分要么装不上，要么装上没用。折腾了3天，最终只筛出5个值得装的。

---

## 为什么要测试这些 Skills？

Claude Code 裸装，只是个能干的终端工具。但装对 Skills，才是把它能力放大的那个乘数。

我看到很多推荐文章，什么"必装12个"、"效率翻倍"，看着都很诱人。但实际上手才发现——**能顺利装上、真正好用的，少得可怜**。

---

## 我的测试标准

装一个 Skill 之前，我会看这4点：

1. **10分钟能装好吗？** 依赖一大堆、报错一大片的，直接pass
2. **文档清楚吗？** 看不懂怎么用的，再牛也没用
3. **真的有效果吗？** 承诺的功能能实现吗？
4. **会常用吗？** 装完吃灰的工具，等于没装

按这个标准筛下来，**90%都被刷掉了**。

---

## 通过测试的5个

### 1. caveman - 省65% token

**它是什么**  
一个 token 压缩工具。用"穴居人"式的简短说话方式，把同样的信息塞进更少的 token。

**解决什么问题**  
Claude Code 跑长任务时，context 很容易烧光。烧光了就得清上下文、丢历史。caveman 用极简措辞输出，能省约65%的 token。

**安装体验**  
一键脚本，非常顺滑：
```bash
curl -fsSL https://raw.githubusercontent.com/JuliusBrussee/caveman/main/install.sh | bash
```

自动识别你机器上的所有 AI 助手（Claude Code、Codex、OpenClaw 等），全部装好。我装完后发现多了20个 skills，包括 caveman 主体、caveman-compress、caveman-review 等。

**适合谁用**  
所有人。只要你跑长任务、长对话，省下来的 token 就是省下来的钱。

**推荐指数**  
⭐⭐⭐⭐⭐

---

### 2. graphify - 代码库知识图谱

**它是什么**  
把代码库转成可查询的知识图谱。AI 能看到函数调用关系、类继承结构、文件依赖，而不是盲目地在一堆代码里瞎找。

**解决什么问题**  
大型项目是 AI 编程的最大障碍——上下文塞不下，AI 看不全就乱改。graphify 把代码库结构化成图谱，AI 查关系、追调用、定位改动点都有了准头。

**安装体验**  
需要 Python，但安装很简单：
```bash
pip install graphifyy      # 注意是双y
graphify install           # 注册到 AI 助手
```

装完后，在项目里运行 `/graphify .` 就能生成知识图谱。

**适合谁用**  
大项目必备。代码库超过1万行的，强烈推荐。小项目用处不大。

**推荐指数**  
⭐⭐⭐⭐⭐（大项目）  
⭐⭐⭐（小项目）

---

### 3. OpenSpec - 规格驱动开发

**它是什么**  
让 AI 编程从"对话式临场发挥"变成"先写 spec、再按 spec 实现"。需求落成可读、可追踪的规格文档，AI 按文档一步步实现。

**解决什么问题**  
AI 编程最大的坑不是写不出代码，是**写出来的代码对不对没法验证**。OpenSpec 先约定清楚要做什么，再让 AI 照着做，每步可验证。

**安装体验**  
需要 Node.js 20+，全局安装：
```bash
npm install -g @fission-ai/openspec@latest
cd your-project
openspec init
```

装完后，在项目里用 OpenSpec 管理需求、设计、任务。

**适合谁用**  
做正经项目的人。写一次性脚本不需要，做产品级开发必备。

**推荐指数**  
⭐⭐⭐⭐⭐（产品开发）  
⭐⭐（一次性脚本）

---

### 4. karpathy-skills - Karpathy 避坑清单

**它是什么**  
一个配置文件。Andrej Karpathy 对"LLM 写代码常踩哪些坑"的观察，直接写进 Claude Code 的行为规则里。

**解决什么问题**  
AI 写代码有些常见坑：重复造轮子、过度抽象、忽略边界条件等。这份清单把这些反模式直接告诉 AI，让它主动避开。

**安装体验**  
Claude Code 插件方式，两条命令：
```bash
claude plugin marketplace add forrestchang/andrej-karpathy-skills
claude plugin install andrej-karpathy-skills@karpathy-skills
```

装完后，AI 的行为会自动遵循这些规则。

**适合谁用**  
所有人。零成本、收益直接，适合任何新项目的起手式。

**推荐指数**  
⭐⭐⭐⭐⭐

---

### 5. claude-hud - 实时监控面板

**它是什么**  
给 Claude Code 加个可视化面板，实时显示上下文用量、当前活动、token 消耗。

**解决什么问题**  
AI 编程最大的失控来源是"不知道它现在占了多少上下文、在哪个环节烧 token"。claude-hud 把这些数据摆出来，你才知道什么时候该清上下文、什么时候该停下来重新对齐。

**安装体验**  
Claude Code 插件方式：
```bash
claude plugin marketplace add jarrodwatts/claude-hud
claude plugin install claude-hud@claude-hud
```

装完后，运行 Claude Code 时会自动显示监控面板。

**适合谁用**  
跑长任务的人。如果你经常遇到"AI 突然不听话"、"token 莫名其妙烧光"，装这个能让你看清发生了什么。

**推荐指数**  
⭐⭐⭐⭐

---

## 那些没通过测试的

测试过程中，我还试了很多其他 Skills：

- **Context7** - 理念很好（实时代码文档），但安装时交互式界面卡住了，折腾半天没装上
- **Playwright MCP** - 需要手动配置 MCP server，不是一键安装，门槛太高
- **Superpowers** - 依赖太多，光装依赖就花了20分钟，最后还报错
- **ECC** - 文档写得云里雾里，看不懂怎么用
- **pua** - 名字太敏感，而且"提高 agent 积极性"这个卖点很虚

这些不是说它们不好，而是**对普通用户来说，装上去的成本太高了**。

---

## 怎么选，别照单全收

看到这里，你可能想："那我把这5个全装上？"

**别。**

Skills 不是越多越好。装多了反而互相冲突、拖慢上下文、让 AI 不知道听谁的。

**我的建议**：

1. **必装2个**：caveman + karpathy-skills  
   零成本、收益直接，适合所有人

2. **按场景选1个**：
   - 大项目 → graphify
   - 正经开发 → OpenSpec
   - 长任务 → claude-hud

3. **用一段时间再加**：  
   别一次性装一堆，先用一段时间，感觉哪里不够再补

---

## 最后说两句

很多人把 Claude Code 当成一个更聪明的命令行工具，装完就开干。

但它的真正价值要在 Skills 生态里才释放出来——**裸装的 Claude Code 是发动机，Skills 是变速箱和方向盘，没有后者你只能在原地轰油门**。

不过，**不是 Star 高就好用，要自己测试才知道**。

这5个是我验证过的，希望能帮你少踩坑。

---

**如果这篇文章对你有帮助，欢迎转发给需要的朋友。**

有问题可以在评论区留言，我会一一回复。

---

> 作者：登哥  
> 专注 AI 工具实战，实测验证不吹牛  
> 公众号：【你的公众号名称】
