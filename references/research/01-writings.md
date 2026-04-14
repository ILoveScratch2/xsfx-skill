# 细数繁星（XSFX）著作与系统性表达调研

## 调研范围

本维度优先使用一手文本：本地文章、学习笔记、洛谷文章摘录，以及 TouchFish/TFv5 的文档型输出。

### 一手来源
- `references\sources\articles\luogu-oi-retirement-akar3ws4.md`
- `references\sources\articles\luogu-touchfish-z6se69kk.md`
- `references\sources\articles\oi-parents-advice.txt`
- `references\sources\articles\block-notes.txt`
- `references\sources\articles\economics-game.txt`
- `references\sources\code\TouchFish\README.md`
- `references\sources\code\TouchFish\LTS.py`

### 二手来源
- 无专门二手人物分析；本人物公开访谈稀缺，本调研尽量不引入外部转述。

### 公开 URL
- https://www.luogu.com.cn/article/akar3ws4
- https://www.luogu.com.cn/article/z6se69kk
- https://github.com/2044-space-elevator/TouchFish
- https://github.com/2044-space-elevator/TFV5_server

---

## 一、可确认的写作母题

### 1. 工程不是炫技，是把系统真的搭起来

- 他不是先谈“我要做一个很酷的软件”，而是先谈**具体场景**：机房断网、同学交流、局域网聊天室。`references\sources\articles\luogu-touchfish-z6se69kk.md:14-29`
- 他会写“真正实现聊天室的功能”“手把手教大家如何使用”，说明他写文档时默认自己要把最后一公里也负责到底。`references\sources\articles\luogu-touchfish-z6se69kk.md:16-18`, `31-60`
- 在 OI 退役文里，TouchFish 的诞生也被写成一个很具体的动作：“花了一下午写完了 TouchFish 的初代版本，招了一个开发组”。`references\sources\articles\luogu-oi-retirement-akar3ws4.md:52-57`

**结论**：XSFX 的长文不是“观点型”优先，而是“把一套东西搭出来”优先。

### 2. 他天然把世界看成规则、角色和账本

- 经济学游戏从第一天就不是随便玩玩，而是“中央账本模式统一管理”“国有银行”“加息”“国债”“上市”“信用卡”“储蓄卡”“坏账处理”的制度化设计。`references\sources\articles\economics-game.txt:1-85`
- TouchFish v4 的开头直接就是协议文档，且把系统切成 `Gate / Chat / Misc` 三块。`references\sources\code\TouchFish\LTS.py:8-18`
- 他的教程写法也类似制度设计：先定义符号，再分类讨论，再给复杂度，再给代码。`references\sources\articles\block-notes.txt:22-62`

**结论**：相比“灵感型创作”，XSFX 更像一个小型制度工程师。

### 3. 他喜欢把复杂问题翻译成普通人能用的话

- 在写给家长和准备入坑 OI 的文章里，他主动说自己在“尽可能转换成了圈外人听得懂的名词”，例如把 “AFo” 改成“暂停信奥的学习”。`references\sources\articles\oi-parents-advice.txt:1-7`
- TouchFish 使用文也是标准的“先拿 IP，再查端口，再开服务端，再让客户端填参数”的平民化步骤。`references\sources\articles\luogu-touchfish-z6se69kk.md:44-60`
- 即便是数据结构笔记，他也会用“这个用初中数学就能证明出来”“分块是暴力中最优雅的”这种带情绪和画面感的句子。`references\sources\articles\block-notes.txt:7`, `39-43`

**结论**：他的写作不是为了显得懂，而是为了让读者跟上。

### 4. 他既热爱技术，也很早就有“投入-回报”意识

- 他对 OI 的根本判断非常直接：如果不是出于兴趣，“我强烈反对你学信奥”。`references\sources\articles\oi-parents-advice.txt:33-39`
- 同时他又明确写“信奥是一个投资大、回报小的东西”，而且临近中考和高考“就要立即停止信奥的学习”。`references\sources\articles\oi-parents-advice.txt:37-39`, `51-53`
- 退役文最后的落点不是浪漫主义，而是“归根到底，就是因为热爱”，但也承认 NOI Ag 以下几乎不产生升学效益。`references\sources\articles\luogu-oi-retirement-akar3ws4.md:80-94`

**结论**：他不是空热爱派，而是“热爱驱动 + 现实记账”。

---

## 二、反复出现的候选心智模型

### A：系统先行

**一句话**：遇到问题先搭角色、规则和状态，再谈功能和体验。

**跨域证据**：
- 班级经济系统：中央账本、国有银行、利率、国债、上市、公务员、坏账。`references\sources\articles\economics-game.txt:7-85`
- 聊天系统：协议版本、角色状态、配置上下限。`references\sources\code\TouchFish\LTS.py:8-35`, `447-455`
- 技术写作：符号约定 → 分类讨论 → 复杂度 → 代码。`references\sources\articles\block-notes.txt:22-62`

**是否通过三重验证**：
- 跨域复现：通过
- 有生成力：通过
- 有排他性：通过

### B：优雅暴力

**一句话**：最优解太重时，先找一个结构清楚、能跑、可扩展的“优雅暴力”。

**跨域证据**：
- 明说“分块是一种暴力，但是不失为暴力中最优雅的”。`references\sources\articles\block-notes.txt:7`
- 数据结构讲解里强调在 `n/B` 和 `B` 之间做平衡，而不是神化最优理论。`references\sources\articles\block-notes.txt:31-43`
- TouchFish 初代“花了一下午写完”，说明他能接受先把核心跑通。`references\sources\articles\luogu-oi-retirement-akar3ws4.md:54-57`

**是否通过三重验证**：
- 跨域复现：通过
- 有生成力：通过
- 有排他性：中高

### C：翻译复杂事

**一句话**：真正掌握一件事，不只是会做，还得能把黑话翻成普通人能执行的动作。

**跨域证据**：
- 主动把 OI 黑话改写成圈外人能理解的词。`references\sources\articles\oi-parents-advice.txt:1-7`
- TouchFish 使用说明是明显的“把工程细节翻译成操作流程”。`references\sources\articles\luogu-touchfish-z6se69kk.md:31-60`
- 连分块笔记都要写“省流”“这很显然”“代码很好写”。`references\sources\articles\block-notes.txt:46-62`

**是否通过三重验证**：
- 跨域复现：通过
- 有生成力：通过
- 有排他性：中

### D：热爱驱动的现实主义

**一句话**：喜欢就去做，但任何投入都必须认账，不能骗自己。

**跨域证据**：
- “热爱”是退役文的最终答案。`references\sources\articles\luogu-oi-retirement-akar3ws4.md:86-94`
- 同时明确 OI 的时间成本、升学边界和停损时机。`references\sources\articles\oi-parents-advice.txt:37-53`
- 暑假“没忍住，去搞工程了”，体现强烈的内驱。`references\sources\articles\luogu-oi-retirement-akar3ws4.md:52-57`

**是否通过三重验证**：
- 跨域复现：通过
- 有生成力：通过
- 有排他性：中

---

## 三、最能代表他写作气质的原句

1. **“分块是一种暴力，但是不失为暴力中最优雅的。”**  
   —— 技术判断里带文学修辞。`references\sources\articles\block-notes.txt:7`

2. **“我也不过一普通人。”**  
   —— 高度自我降格，但不是摆烂。`references\sources\articles\luogu-oi-retirement-akar3ws4.md:92-94`

3. **“对无情的代码有感情是很抽的事。”**  
   —— 典型理工科大文人句式。`references\sources\articles\luogu-oi-retirement-akar3ws4.md:90-92`

4. **“我强烈反对你学信奥！”**  
   —— 写劝导文时又非常直接，几乎不绕。`references\sources\articles\oi-parents-advice.txt:33-39`

5. **“手把手教大家如何使用 TouchFish。”**  
   —— 不是炫项目，而是让别人能落地。`references\sources\articles\luogu-touchfish-z6se69kk.md:33-40`

---

## 四、核心张力

1. **文人修辞 vs 工程落地**  
   一边会写“优雅的暴力”“对无情的代码有感情”，一边又把 IP、端口、协议、利率、坏账写得极具体。`references\sources\articles\block-notes.txt:7`, `references\sources\articles\luogu-touchfish-z6se69kk.md:44-60`

2. **自嘲收敛 vs 野心不小**  
   自称“普通 OIer”，但又会搭班级经济系统、写协议、拉团队、做产品。`references\sources\articles\luogu-oi-retirement-akar3ws4.md:12-16`, `references\sources\articles\economics-game.txt:7-85`

3. **热爱技术 vs 现实停损**  
   明明喜欢，却不断提醒别人别把 OI 当万能升学工具。`references\sources\articles\oi-parents-advice.txt:37-53`, `references\sources\articles\luogu-oi-retirement-akar3ws4.md:80-94`

---

## 五、本维度结论

从“著作与长文”维度看，XSFX 最稳定的写作人格不是“少年天才炫技者”，而是：

1. **把现实问题抽象成系统的人**  
2. **愿意把复杂技术翻译给普通读者的人**  
3. **一边热爱，一边老老实实算代价的人**

这三点和聊天记录、代码文档中的人格高度一致，可信度高。

## 置信度说明

- **高**：系统先行、翻译复杂事、热爱但现实记账
- **中高**：优雅暴力
- **中**：所有“理工科大文人”判断；证据强，但公开长文数量仍有限
