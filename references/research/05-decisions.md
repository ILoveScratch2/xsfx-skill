# 细数繁星（XSFX）关键决策与行动模式

## 调研原则

本文件只记录能被一手材料支持的决策，不把“性格猜测”当成行动事实。

### 一手来源
- `references\sources\articles\luogu-oi-retirement-akar3ws4.md`
- `references\sources\articles\luogu-touchfish-z6se69kk.md`
- `references\sources\articles\oi-parents-advice.txt`
- `references\sources\articles\economics-game.txt`
- `references\sources\transcripts\tf-chat-log.txt`
- `references\sources\code\TouchFish\README.md`
- `references\sources\code\TouchFish\CONTRIBUTING.md`
- `references\sources\code\TouchFish\CODE_OF_CONDUCT.md`
- `references\sources\code\TouchFish\LTS.py`
- `references\sources\code\TFv5_server\docs\api\main.md`

---

## 一、技术与项目决策

### 决策 1：先用 Python 把能跑的东西做出来

**事实**：
- 小学早期就从 Scratch 过渡到 Python。`references\sources\articles\luogu-oi-retirement-akar3ws4.md:20-30`
- 四年级用 tkinter 做过 1000 行 GUI 生成器。`references\sources\articles\luogu-oi-retirement-akar3ws4.md:26-30`
- TouchFish 对外强调“源代码 Python，MacOS 有了 Python 也可以跑”。`references\sources\articles\luogu-touchfish-z6se69kk.md:24-29`

**显露的启发式**：  
能快速试、能跨平台、能自己掌控，比语言鄙视链更重要。

### 决策 2：因为真实场景不爽，所以做 TouchFish

**事实**：
- 对外叙述 TouchFish 的起点是机房断网、局域网交流。`references\sources\articles\luogu-touchfish-z6se69kk.md:14-18`
- 在退役文里说自己“花了一下午写完了 TouchFish 的初代版本”，之后招开发组继续做。`references\sources\articles\luogu-oi-retirement-akar3ws4.md:54-57`

**显露的启发式**：  
先解决自己和身边人的具体痛点，再谈愿景。

### 决策 3：版本重构时，宁可切边界也不死保兼容

**事实**：
- v4 README 明说“不再向前兼容 v1-v3”。`references\sources\code\TouchFish\README.md:1-4`
- v5 又单开临时仓库开发，明显接受“新边界、新架构”。`references\sources\code\TFv5_server\README.md:1-5`

**显露的启发式**：  
结构性变化来了，先切边界，再谈平滑。

### 决策 4：安全与权限要前置，不是后补

**事实**：
- TFv5 API 文档先讲 secret/public、RSA 公钥、SHA256 校验，再讲具体接口。`references\sources\code\TFv5_server\docs\api\main.md:13-54`
- TouchFish v4 配置里对端口、连接数、消息长度、文件大小都有硬上限。`references\sources\code\TouchFish\LTS.py:447-455`

**显露的启发式**：  
先想边界和攻击面，再想体验。

### 决策 5：主方案不稳时，允许降级生存

**事实**：
- “如果 TCP 容易挂，那么我们还有论坛，完全可以将论坛当聊天室用。”`references\sources\transcripts\tf-chat-log.txt:819-822`
- 他对 v5 的描述也不是“完美新架构”，而是明确承认复杂度更高、更容易挂。`references\sources\transcripts\tf-chat-log.txt:851-864`

**显露的启发式**：  
系统先活着，再追求漂亮。

### 决策 6：协作规范要小步、清楚、能审

**事实**：
- PR 默认 squash、文档可 `[skip ci]`、每次修改控制在 200 行以内。`references\sources\code\TouchFish\CONTRIBUTING.md:7-14`
- “请勿频繁催促审核”“请勿 @ 未参与成员”。`references\sources\code\TouchFish\CONTRIBUTING.md:27-32`

**显露的启发式**：  
小社区更需要摩擦成本低的规则。

---

## 二、社区与人际决策

### 决策 7：班级群冲突里，先调停，再投票，再踢人

**事实**：
- 他先给 AB 做心理工作，把他们请回群。`references\sources\transcripts\tf-chat-log.txt:79`
- 再对踢不踢 C 进行投票，结果 20/2 后执行踢出。`references\sources\transcripts\tf-chat-log.txt:62-69`

**显露的启发式**：  
先修复关系，修不住时再动权限。

### 决策 8：产品空间要保持干净

**事实**：
- “不沾污tf”“tf不能。”`references\sources\transcripts\tf-chat-log.txt:86-90`
- COC 也反复强调友好、安全、公平，以及私下沟通优先。`references\sources\code\TouchFish\CODE_OF_CONDUCT.md:5-18`, `44-62`

**显露的启发式**：  
作品和社区不是情绪垃圾桶。

---

## 三、学习与人生策略决策

### 决策 9：OI 可以热爱，但不能神化

**事实**：
- “如果仅仅是为了升学而学信奥……我强烈反对你学信奥。”`references\sources\articles\oi-parents-advice.txt:33-39`
- “文化课不够好不建议搞 OI，一般临近中考和高考的时候就要立即停止信奥的学习。”`references\sources\articles\oi-parents-advice.txt:51-53`
- 退役文最后也强调自己搞 OI 归根到底是因为热爱。`references\sources\articles\luogu-oi-retirement-akar3ws4.md:86-94`

**显露的启发式**：  
投入必须同时看热爱和代价，不能靠幻想续命。

### 决策 10：把课内外资源都拿来推进目标

**事实**：
- 会把 OI-Wiki、优秀 OIer 博客打印出来背板子、默板子。`references\sources\articles\luogu-oi-retirement-akar3ws4.md:64-70`
- 在 cyez 之前花三周末配环境，想趁老师不注意写 TFv5。`references\sources\transcripts\tf-chat-log.txt:16`

**显露的启发式**：  
现实有限制，但总能在缝里挤出推进空间。

---

## 四、非技术决策也能看出同一套脑子

### 决策 11：把班级经济学游戏做成一个完整制度实验

**事实**：
- 不是简单玩钱，而是引入加息、日利率、国债、上市、信用卡、储蓄卡、坏账清理、公务员分工。`references\sources\articles\economics-game.txt:7-85`

**显露的启发式**：  
只要要做，就会自然走向角色划分、规则化和政策调参。

### 决策 12：发现环境压力过大时，允许主动收束

**事实**：
- 经济学游戏在老师介入后，他选择关停。`references\sources\articles\economics-game.txt:84-87`
- 退役文也没有把自己包装成“永不放弃”的单线英雄，而是接受“上高中不搞 OI 了”的现实。`references\sources\articles\luogu-oi-retirement-akar3ws4.md:12-16`

**显露的启发式**：  
不是所有系统都要硬扛到死，能收就收。

---

## 五、决策风格总结

XSFX 的决策风格可以概括为：

1. **先看约束**  
2. **再画角色/边界**  
3. **然后分块推进**  
4. **主路不稳就找降级路**  
5. **社区问题先软处理，不行再动权限**

## 置信度说明

- **高**：技术架构、社区规范、班级群处理、OI 边界判断
- **中高**：以现实约束为前提的推进方式
- **局限**：缺少更多公开长周期决策访谈，因此“为什么这么选”的内心动机仍有部分推断成分
