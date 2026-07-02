# 计算机精进总路线图：六语言大师 + 财务独立

> "武器是战争的重要因素，但不是决定的因素，决定的因素是人不是物。力量对比不但是军力和经济力的对比，而且是人力和人心的对比。军力和经济力是要人去掌握的。"  
> —— 毛泽东《论持久战》

> 翻译：语言是武器，但不是决定因素。决定因素是你自己。工具和资源是量，你的认识和实践是质。

---

## 总纲

### 核心矛盾

你的终极目标与当前资源的矛盾。你想学所有语言、理解计算机全部、做到财务独立——但一天只有 24 小时。

### 解决矛盾的方法

**战略上以一当十，战术上以十当一。**  
—— 长期（10 年）要覆盖六种语言和完整计算机领域知识。当下（每周）专注一个 pattern、一种语言的深度。

### 三大原则

1. **实践驱动认识**——不做练习题、不看书打代码。每个知识点的理解必须通过在你仓库中写出可跑通的 exercise 来验证。
2. **逐步扩大根据地**——先精通 2-3 个语言，再拓展到其他。不要同时学 6 个语言，那必然是失败的。
3. **在战争中学习战争**——通过实际解决开源 issue、完善自己仓库来学习，不是"学完再做"。

---

## 第一部：路线全景图（10 年视野）

```
时间轴   语言重心         仓库建设           开源贡献        商业化
─────────────────────────────────────────────────────────────
第1年    TS+Python为主     完 46 pattern       修自己的issue     不碰
         Rust开始         CI/CD完善           提出issue 
         
第2年    Rust+Go开始       生产级别代码        交第1个外部PR     订阅/赞助
         深入C            exercise4语言完      参与社区
         
第3年    C深入             写新pattern          维护1-2库        开咨询
         全部6语言读生产                             
         
第4-5年  精通主2门         出版/课程            成为 maintainer   SaaS MVP

第6-10年 全栈+深专          做独立产品           核心 maintainer   财务基本自由
```

### 第一年：巩固根据地

**目标**：用你已经有的仓库和 4 种语言（TS/Python/Rust/Go/C）各完成至少 30 个 pattern 的 implementations。每个语言都能独立写出一个完整 pattern。

### 第二到三年：战略反攻

**目标**：精通 2-3 门语言达到生产级水平。开始向上游贡献代码，在社区建立声望。

### 第四到五年：建立统一战线

**目标**：成为某个领域的公认专家（如分布式系统模式、并发编程模式、系统编程模式）。开始独立商业化探索。

### 第六到十年：战略决战

**目标**：要么你的开源产品/项目/社区达到 thousand 级别影响力，要么你的商业化项目实现财务独立。

---

## 第二部：每种语言的学习路径

> 策略要点：**先精后广**。第一年专注 TS + Python + Rust 三门。
> Go 和 C 放在第二年深入概念基础后。

### 一、TypeScript（第1年攻占）

| 阶段 | 学习内容 | 你仓库的应用 | 验证方式 |
|------|---------|------------|---------|
| 基础（1个月） | 类型系统（泛型、联合、交叉、映射） | 改写你的 exercise 用更严格的 TS 类型 | `pnpm test:ts` |
| 进阶（2个月） | 异步、装饰器、Conditional Types | 在你的 circuit-breaker 做高级类型体操 | Code Review |
| 深入（3-6月） | 编译器 API、`tsconfig` 全部选项 | 学 VitePress 配置机制 | 看 VitePress源码 |
| 源码级 | TypeScript 编译器源码 | 读 checker.ts | 写博客解读 |

**权威资源**：
1. [TypeScript Handbook](https://www.typescriptlang.org/docs/) —— 官方，任何时候都是第一参考
2. [TypeScript Deep Dive](https://basarat.gitbook.io/typescript/) —— 免费书，比官方更深入
3. [TypeScript 编译器源码](https://github.com/microsoft/TypeScript) —— 最终答案
4. [Type Challenges](https://github.com/type-challenges/type-challenges) —— 类型体操练习
5. [Effective TypeScript](https://effectivetypescript.com/) —— Dan Vanderkam 的书，第三版正在写

### 二、Python（第1年攻占）

| 阶段 | 学习内容 | 你仓库的应用 | 验证方式 |
|------|---------|------------|---------|
| 基础（1个月） | Pythonic 写法、类型标注（typing） | 改写你的 Python exercise | `pytest` |
| 进阶（2个月） | 生成器、协程、`asyncio`、上下文管理器 | 在你的 pattern 里用 asyncio | 性能对比 |
| 深入（3-6月） | CPython 源码、GIL、`ctypes`、C 扩展 | 了解每个 pattern 在动态语言下的特性 | 写 PyCon 风格的文章 |

**权威资源**：
6. [Python 官方教程](https://docs.python.org/3/tutorial/) —— 基础
7. [Fluent Python](https://www.oreilly.com/library/view/fluent-python-2nd/)，Luciano Ramalho —— 进阶必读
8. [Python Cookbook](https://www.oreilly.com/library/view/python-cookbook-3rd/)，David Beazley —— 实战
9. [CPython Internals](https://realpython.com/products/cpython-internals-book/) —— 解释器内部
10. [Architecture Patterns with Python](https://www.cosmicpython.com/) —— DDD 和 TDD
11. [Talk Python To Me](https://talkpython.fm/) 播客 —— 保持前沿视野
12. [PEP 8](https://peps.python.org/pep-0008/) —— 风格规范
13. [Awesome Python](https://github.com/vinta/awesome-python) —— 生态名录

### 三、Rust（第1年下半年开始，持续到第3年）

| 阶段 | 学习内容 | 你仓库的应用 | 验证方式 |
|------|---------|------------|---------|
| 基础（2个月） | 所有权、借用、生命周期、模式匹配 | 重写 Rust exercises 做到无 unsafe | `cargo test` `cargo clippy` |
| 进阶（2个月） | trait、泛型、迭代器、闭包、并发（Send/Sync） | 给 10 个 pattern 用 Rust 实现并发版本 | 无 unsafe 警告通过 |
| 深入（3-6月） | unsafe、FFI、proc macro、Pin、Future | 写一个 Rust proc macro | 编译通过 |
| 源码级 | rustc 编译器、标准库 | 读 std/src 源码 | 写系列博客 |

**权威资源**：
14. [The Rust Book](https://doc.rust-lang.org/book/) —— 入门唯一资源
15. [Rust by Example](https://doc.rust-lang.org/stable/rust-by-example/) —— 代码示例
16. [Rust Standard Library 源码](https://github.com/rust-lang/rust/tree/master/library/std) —— 最终权威
17. [Programming Rust](https://www.oreilly.com/library/view/programming-rust-2nd/)，Jim Blandy —— O'Reilly 权威书
18. [Rustonomicon](https://doc.rust-lang.org/nomicon/) —— unsafe Rust 唯一指南
19. [Rust Design Patterns](https://rust-unofficial.github.io/patterns/) —— 与你的仓库直接相关
20. [Learn Rust With Entirely Too Many Linked Lists](https://rust-unofficial.github.io/too-many-lists/) —— 所有权最佳学习
21. [Command line apps in Rust](https://rust-cli.github.io/book/) —— 实战练习
22. [Rust Atomics and Locks](https://marabos.nl/atomics/) —— Mara Bos 的并发书
23. [This Week in Rust](https://this-week-in-rust.org/) —— 每周关注生态

### 四、Go（第2年）

| 阶段 | 学习内容 | 你仓库的应用 | 验证方式 |
|------|---------|------------|---------|
| 基础（1个月） | 语法、goroutine、channel、interface | 改写 Go exercise | `go test` |
| 进阶（2个月） | 并发模式（pipeline、fan-in/out）、`sync`包 | 给 10 个 pattern 加 Go 并发版本 | `go vet` `-race` 通过 |
| 深入（3-6月） | GC、调度器、pprof、trace | 性能分析自己的代码 | `go tool pprof` |
| 源码级 | Go runtime 源码 | 读 runtime 调度器和 GC | 写源码分析 |

**权威资源**：
24. [The Go Programming Language](https://www.gopl.io/)，Donovan & Kernighan —— 唯一入门书
25. [Effective Go](https://go.dev/doc/effective_go) —— 官方权威风格指南
26. [Go by Example](https://gobyexample.com/) —— 快速参考
27. [Concurrency in Go](https://www.oreilly.com/library/view/concurrency-in-go/9781491941294/)，Katherine Cox-Buday
28. [Go 标准库源码](https://github.com/golang/go/tree/master/src) —— 最终答案
29. [Go 调度器源码分析](https://github.com/golang/go/blob/master/src/runtime/proc.go)
30. [Go Memory Model](https://go.dev/ref/mem) —— 并发内存模型
31. [Go 编译器源码](https://github.com/golang/go/tree/master/src/cmd/compile)
32. [The Go Blog](https://go.dev/blog/) —— 官方博客，权威

### 五、C（第2-3年）

| 阶段 | 学习内容 | 你仓库的应用 | 验证方式 |
|------|---------|------------|---------|
| 基础（1-2月） | 指针、内存管理、结构体、宏 | 在 exercises 里增加 C 实现 | `gcc -Wall -Wextra` 无警告 |
| 进阶（3月） | 函数指针、可变参数、setjmp/longjmp、信号 | 用 C 实现 10 个模式 | Valgrind 无泄漏 |
| 深入（6月） | POSIX API、多线程(pthreads)、网络编程 | 写一个 mini libc | 无 UB |
| 源码级 | Linux 内核、glibc、redis、sqlite | 读内核调度器、内存管理 | 写分析系列 |

**权威资源**：
33. [The C Programming Language](https://www.amazon.com/Programming-Language-2nd-Brian-Kernighan/dp/0131103628)（K&R）—— 圣经
34. [Computer Systems: A Programmer's Perspective](http://csapp.cs.cmu.edu/)，Bryant & O'Hallaron（CS:APP）—— 理解计算机系统的唯一必读
35. [The Linux Programming Interface](https://man7.org/tlpi/)，Michael Kerrisk —— Linux API 权威参考
36. [Advanced Programming in the UNIX Environment](https://www.amazon.com/Advanced-Programming-UNIX-Environment-3rd/dp/0321637739)（APUE）
37. [Beej's Guide to Network Programming](https://beej.us/guide/bgnet/) —— 网络编程标准入门
38. [Modern C](https://modernc.gforge.inria.fr/)，Jens Gustedt —— C11 新标准
39. [C Traps and Pitfalls](https://www.amazon.com/Traps-Pitfalls-Andrew-Koenig/dp/0201179288)，Andrew Koenig
40. [Expert C Programming: Deep C Secrets](https://www.amazon.com/Expert-Programming-Peter-Linden/dp/0131774298)，Peter van der Linden

### 六、算法 & 系统（贯穿全程）

这些不属于单一语言，但你的仓库 46 个 pattern 中至少 30 个属于此领域。

**权威资源**：
41. [Introduction to Algorithms](https://mitpress.mit.edu/books/introduction-algorithms-fourth-edition)（CLRS）—— 算法教材
42. [The Algorithm Design Manual](https://www.algorist.com/)，Skiena —— 更实战
43. [Operating Systems: Three Easy Pieces](https://pages.cs.wisc.edu/~remzi/OSTEP/)（OSTEP）—— 免费，操作系统入门
44. [Designing Data-Intensive Applications](https://dataintensive.net/)，Martin Kleppmann —— 分布式系统唯一必读
45. [Computer Networking: A Top-Down Approach](https://www.amazon.com/Computer-Networking-Top-Down-Approach-7th/dp/0133594149)，Kurose & Ross

---

## 第三部：学习方法论（如何学）

### 毛泽东实践论之学习三步法

```
读源码（理论） → 复现/修改（实践） → 写进自己仓库（再认识）
    ↑                                           │
    └───────────────────────────────────────────┘
                   螺旋上升
```

**应用到具体模式**：

以你刚完成的 circuit-breaker 为例：
1. **读源码** —— 读 Hystrix、Resilience4j、gobreaker 源码
2. **复现/修改** —— 修复 Q3 答案
3. **写进自己仓库** —— 更新 en + zh，加 production proof，CI 验证
4. **认识上升** —— 下次你再遇到并发控制问题，你会想到 CAS + permit 两层

### 学习节奏

| 粒度 | 节奏 | 产出 |
|------|------|------|
| 每天 | 1-2 小时编码 | 至少 1 个 commit |
| 每周 | 深入 1 个 pattern | 理解 1 个 pattern 在 4 语言中的实现差异 |
| 每月 | 1 个跨语言专题 | 博客文章 / 演讲 / 源码分析 |
| 每季 | 1 个语言大版本 | `cargo test` `go test` `pytest` `pnpm test:ts` 全通过 |
| 每年 | 1 个领域突破 | 交 PR / 发课程 / 做产品 |

### 刻意练习原则

根据 Ericsson 1993 和 Norvig 的十原则，你的练习必须满足：

1. **有明确目标**（不是"学Rust"，是"用Rust实现一个无unsafe的 LRU cache"）
2. **有即时反馈**（编译器错误、测试失败、code review）
3. **在舒适区之外**（当你觉得"这个模式我用TS写过了，Rust也就是换个语法"时——你在舒适区）
4. **重复优化**（不是写一次，是写三次：第一版跑通，第二版优化，第三版用最地道的方式）

---

## 第四部：检验标准（如何知道学会了）

> 没有检验标准的学习计划等于没有计划。

### 每项技能的检验标准

| 语言 | 初级（第1年） | 中级（第2-3年） | 高级（第4-5年） |
|------|-------------|---------------|---------------|
| TypeScript | 你的仓库 46 pattern 全类型安全 | 实现了 1 个 VitePress 插件 | 给 DefinitelyTyped 交了 PR |
| Python | 你的仓库 46 pattern pytest 全过 | 用 asyncio 重写了 10 个模式 | 给 CPython 交过 PR |
| Rust | 你的仓库 Rust exercise 全过 | 无 unsafe 实现了 20 个模式 | 给 Rust std 库交过 PR |
| Go | 你的仓库 Go exercise 全过 | 用 goroutine 实现了 10 个模式 | 给 Go 标准库交过 PR |
| C | 你的仓库有 C 实现 | 实现了一个 mini libc | 给 Linux kernel 或 redis 交过 PR |

### 终身检验

每年年底回头问自己三个问题：

1. **去年我的仓库有多少新加的内容？** 如果少于 10 个 pattern 级别的贡献，说明在退步。
2. **去年我给哪些上游项目交了 PR？** 如果为 0，说明没有跳出自己的舒适区。
3. **去年我从我的知识中获得了多少收入？** 即使只有 $100，说明你的知识产生了价值。如果为 0，思考原因。

---

## 第五部：开源贡献路线图

### 第一阶段：寄生（你的仓库是起点）

以你的仓库为基地，每种语言的 exercise 就是你在那个语言的训练场。不需要找外面的项目做。

### 第二阶段：共生（与上游交互）

当你对某个 pattern 理解足够深时（比如你现在的 circuit-breaker），你会自然发现上游项目的 issue、bug、改进点。

| 进展 | 行动 | 目标项目 |
|------|------|---------|
| 发现文档错误 | 提 PR 修文档 | 你引用的所有项目 |
| 发现测试不充分 | 加一个测试用例 | resilience4j、gobreaker |
| 发现实现问题 | 提 issue + fix PR | 需要到达高级阶段 |

### 第三阶段：主场（成为维护者）

当你持续对一个领域（比如"并发控制 pattern"）投入 2-3 年，你自然被认可。

---

## 第六部：财务独立路线图

> "发展经济，保障供给，是我们的经济工作和财政工作的总方针。"  
> —— 毛泽东《抗日时期的经济问题和财政问题》

### 财务独立三阶段

| 阶段 | 收入形式 | 目标金额 | 时间预期 |
|------|---------|---------|---------|
| 第一阶段 | GitHub Sponsors + 技术咨询 | $500-2000/月 | 第2-3年 |
| 第二阶段 | 知识产品（课程/书/会员） | $2000-10000/月 | 第4-5年 |
| 第三阶段 | SaaS 产品 | $10000+/月 | 第6-10年 |

### 第一阶段：赞助 + 咨询（第2-3年）

- GitHub Sponsors：当你的项目 star > 500，自然有人赞助
- 技术咨询：当你在某个领域（比如你的 pattern 知识库）有不可替代的知识，企业愿意付费咨询
- **如何启动**：把你的仓库做成一个"某某 pattern 大全"的品牌，在知乎/掘金/X 上建立技术影响力

### 第二阶段：知识产品（第4-5年）

把你的 46 个 pattern 变成产品：
- **电子书**：《Battle-Tested Patterns: From Source Code to Production》
  - 不是翻译文档，是结合源码分析和多语言对比的深度内容
  - Leanpub / Gumroad 出版
- **视频课程**：每个 pattern 一个视频，对比四种语言实现
  - 这是你的核心竞争力——没有人做跨四种语言的 pattern 课
- **付费订阅**：每周深度分析一个 pattern 的新生产案例

### 第三阶段：SaaS 产品（第6-10年）

基于你的 pattern 知识做工具：
- **代码审查工具**：自动检测项目中违背某种 pattern 的代码
- **pattern 适配咨询 SaaS**：企业迁移到某个架构时，你提供 pattern 建议

**你是要提供工具，还是提供判断？** 工具更好规模化，判断更有护城河。第一版做工具，后续升级做判断。

---

## 第七部：你仓库的规划（这是你的核心资产）

### 第1年：46 个 pattern 补完 + 完善

- [ ] 每个 pattern 四种语言的 exercise 可运行
- [ ] 每个 pattern 的 Challenge Questions 有参考答案
- [ ] CI 100% 通过、deploy 正常、SEO 有效

### 第2年：深度

- [ ] 选 5-10 个核心 pattern 做深度分析(博客/源码分析)
- [ ] Production Proof 至少每个 pattern 有 3 个生产引用
- [ ] 开始对比不同语言对同一 pattern 的实现差异（这是你的独特价值）

### 第3年：影响力

- [ ] 仓库 star > 1000
- [ ] 建立社区（GitHub Discussions / Discord）
- [ ] 启动 Newsletter / 每周 Pattern

### 第4-5年：品牌

- [ ] 出版电子书（基于仓库内容）
- [ ] 发布课程
- [ ] 开始接受企业培训/咨询

### 第6-10年：产品化

- [ ] 推出 SaaS 工具
- [ ] 达到财务独立

---

## 第八部：你的第一个 100 天实战计划

> 对计划的检验是实践。以下是你的第一个 100 天要做的事。

### 第1-30天：仓库基建

- [ ] 确认所有 46 个 pattern 的 exercise 在 4 种语言都能跑通
- [ ] 跑 `pnpm check:content` 修复所有结构问题
- [ ] 修复所有 open issue
- [ ] 关闭可关闭的 PR

### 第31-60天：深度一个领域

选 1-2 个你感兴趣的 pattern（建议 circuit-breaker 你已经做了，接下来选 retry-backoff 或 consistent-hashing）：

- [ ] 读该 pattern 相关的 5 篇论文
- [ ] 读 3 个生产级实现的源码
- [ ] 写出跨语言的对比分析
- [ ] 更新生产引用
- [ ] 发一篇博客

### 第61-100天：开源突破

- [ ] 给你引用的某个项目（Hystrix / Resilience4j / gobreaker / Redis / PostgreSQL）提交你的第一个 issue
- [ ] 尝试修复该 issue
- [ ] 如果内部项目没有合适的 issue，给你的仓库加一个"跨语言对比"的深度内容 feature

### 每天必须做的事

- 用你的五种语言之一在仓库里至少写 30 分钟代码
- 读 15 分钟权威源码
- 写 5 分钟学习笔记（GitHub issue / 博客 draft）

---

## 第九部：书籍/论文核心必读清单

按优先级排列：

### S级（3-6个月内必读）

| 优先级 | 书名 | 为何必读 |
|--------|------|---------|
| S | [Teach Yourself Programming in Ten Years](https://norvig.com/21-days.html) | 学习的起点 |
| S | [Designing Data-Intensive Applications](https://dataintensive.net/) | 分布式系统圣经 |
| S | [Computer Systems: A Programmer's Perspective](http://csapp.cs.cmu.edu/) | 理解整个计算机栈 |
| S | [Operating Systems: Three Easy Pieces](https://pages.cs.wisc.edu/~remzi/OSTEP/) | OS 入门 |
| S | [Introduction to Algorithms](https://mitpress.mit.edu/books/introduction-algorithms-fourth-edition) | 算法基石 |
| S | Rust Book / The Go PL / Fluent Python | 按你当前学习的语言同步读 |

### A级（1年内读完）

| 书名 | 领域 |
|------|------|
| [Structure and Interpretation of Computer Programs](https://mitpress.mit.edu/sites/default/files/sicp/index.html) | 编程思维整体 |
| [The Art of Learning](https://www.joshwaitzkin.com/the-art-of-learning) | 学习方法 |
| [Peak: Secrets from the New Science of Expertise](https://www.amazon.com/Peak-Secrets-New-Science-Expertise/dp/0544947223) | 刻意练习 |
| [Deep Work](https://www.calnewport.com/books/deep-work/) | 深度工作 |
| [The Pragmatic Programmer](https://pragprog.com/titles/tpp20/) | 编程实践 |
| [The Effective Engineer](https://www.effectiveengineer.com/) | 工程效率 |
| [Zero to One](https://www.amazon.com/Zero-One-Notes-Startups-Future/dp/0804139296) | 创业思维 |
| [翻译毛泽东选集](https://www.marxists.org/reference/archive/mao/works/red-book/) —— (实践论、矛盾论、论持久战) | 战略思维 |

---

## 第十部：你如何知道自己走对了路

### 正确的信号

- 你每天在仓库有 commit
- 你每周会想"哦，这个 pattern 其实可以用那个语言更优雅地表达"
- 你每月写完一篇源码分析后，自己都觉得很深刻
- 你每季度发现"三个月前的我写的代码真差"
- 你每年回头看，自己对这个领域的理解发生了质变

### 错误的信号

- 你在做已经会的东西——那不是练习，是舒适区
- 你 2 周没有 commit —— 失去节奏
- 你只看不写 —— 假性学习
- 你想学的语言 > 3 门同时进行 —— 分散兵力
- 你觉得"等学好了再开始" —— 永远不会有那一天

---

## 第零条：一切开始于现在

你不需要买课。你不需要等到周末。你不需要"准备学习环境"。

你的环境已经就绪：一台 MacBook，一个 GitHub 仓库，46 个 pattern 的打桩，四个语言的工具链，CI/CD 管道。

你现在要做的不是准备，是**开始每天的实践循环**。

> "学习的敌人是自己的满足，要认真学习一点东西，必须从不自满开始。对自己，"学而不厌"，对人家，"诲人不倦"，我们应取这种态度。"  
> —— 毛泽东《中国共产党在民族战争中的地位》

---

**下一步行动**：
- 读完这个计划
- 打开你的 `claude.code`，开始今天的 `pnpm dev`
- 从问题"我如何让这个 pattern 在四个语言中都更地道"开始
