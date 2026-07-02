# 五年精进总路线图：从前端工程师到六语言全栈系统专家

> 背景：软件工程本科毕业（2022届），前端工程师在职，有 C/Python 基础，零 Rust/Go/Java。
> 目标：5年精通6语言（TS/JS, Python, Go, Rust, C, 主攻一门语言后端建设）+ 计算系统核心理解 + 有影响力的开源贡献 + 财务独立探索。

---

## 认识论框架

### 你的五个认识层级

```
第一层（第1年）：工具体 —— 能用那门语言完成常规任务（你现在的前端水平）
第二层（第2年）：生产者 —— 能写出生产级代码，理解惯用法和最佳实践
第三层（第3年）：解剖者 —— 能读懂该语言核心库/运行时的源码
第四层（第4年）：贡献者 —— 能给该语言的生态核心项目提有效 PR
第五层（第5年）：设计者 —— 能设计框架/工具/库，被他人引用
```

你不是要学 6 个语言，而是要在每个语言上都达到至少第三层，在 2-3 个上达到第四到五层。

### 矛盾论

你的主要矛盾是：**有限的全职工作时间与庞大的知识体系之间的矛盾。**

解决方法：**集中优势兵力，各个歼灭敌人。** 每个阶段只攻一个主要方向，辅助方向只要维持即可。

### 战略分期

| 时期 | 主题 | 主攻语言 | 其他语言 |
|------|------|---------|---------|
| 第一年（第一期） | 跳出前端，重构基础 | **Go + Python 深化** | TS 维持 |
| 第二年（第二期） | 攻占系统层 | **C 深入 + Rust 入门** | Go 持续 |
| 第三年（第三期） | 双线作战 | **Rust 精通 + TypeScript 架构** | 全部六语言 |
| 第四年（第四期） | 融会贯通 | **开源主力贡献** | 全部 |
| 第五年（第五期） | 独立自主 | **商业化/产品化** | 全部 |

---

## 六种语言的学习序列设计

```
         前端基础（你在这里）
         TS/JS
        /      \
     Python     Go
       |        |
       C     (中间层)
       |
     Rust
```

**为什么是这个顺序：**

1. **Go（第一年）**—— 从你熟悉的前端后端化，Go 是后端最简单的语言。goroutine、channel 教并发模型，从 JS 的单线程到 Go 的 CSP 是认知转换的绝佳第一步。同时 Go 和 TypeScript 在理念上有相似之处（接口、组合优于继承、结构类型），过渡平滑。
2. **Python 深化（第一年）**—— 你已经学过 Python，这里要做的事情是：从"能写"到"能写出系统级工具"。Python 教元编程、动态特性、C 扩展接口（ctypes），为后面学 C 打基础。
3. **C（第二年）**—— 理解计算机系统的必由之路。指针、内存布局、ABI、栈帧——这些是所有语言底层的共同语言。学完 C，你对 Rust 的 ownership、Go 的 GC、Python 的 GIL 的理解都会发生质变。
4. **Rust（第二年下半年到第三年）**—— Rust 是 C 的现代继承者。所有权和生命周期在学完 C 之后变得直观。Rust 是目前系统编程的事实标准（Linux 内核、浏览器引擎、云基础设施）。
5. **TS/JS 架构深化（第三年）**—— 不是学语法，而是学生态系统的大工程架构（V8 引擎、TypeScript 编译器、前端框架设计哲学）。
6. **Java/C++（可选项，第四年）**—— 视你走向决定。如果走向云基础设施和分布式系统，Java 必学（Kafka、Hadoop、ZooKeeper）。如果走向系统编程和工具链，C++必学（LLVM、TensorFlow 底层、游戏引擎）。

---

## 第一年：重构基础

### 当前起点评估

| 领域 | 当前水平 | 需要 |
|------|---------|------|
| TypeScript/JS | 工作语言，前端工程 | 后端和系统能力 |
| Python | 基础语法 | 系统编程、元编程 |
| Go | 零基础 | 从头开始 |
| Rust | 零基础 | 明年开始 |
| C | 大学基础（已生疏） | 明年开始 |
| 操作系统 | 大学基础 | 深入理解 |
| 网络 | 前端层面（HTTP） | TCP/IP、协议 |
| 数据结构/算法 | 大学基础 | 用多种语言实践 |
| 数据库 | 基础 | 深入理解 |

### 第一年学习日历

#### Q1（第1-3个月）：Go 入门 + 数据结构/算法重修

**学习目标**：能独立用 Go 写出 CRUD 后端 + 命令行工具。用 Go 实现 30 道 LeetCode 中等题。

**学习内容**：
- Go 基础语法（变量、控制流、函数、结构体、接口、错误处理）
- Go 并发（goroutine、channel、select、sync 包）
- Go 标准库（net/http、io、context、flag、testing）
- 数据结构重建（链表、栈、队列、树、图、哈希表）—— 用 Go 各实现一遍
- 算法重点（排序、搜索、动态规划、图算法）—— 用 Go 每天 1 题

**核心资源**：
1. [The Go Programming Language](https://www.gopl.io/)，Donovan & Kernighan —— 唯一的官方权威书，习题必做
2. [Effective Go](https://go.dev/doc/effective_go) —— 官方惯用法
3. [Go by Example](https://gobyexample.com/) —— 快速参考，每天跑一遍
4. [Tour of Go](https://go.dev/tour/) —— 官方入门
5. [Go 标准库文档](https://pkg.go.dev/std) —— 最终权威
6. [Concurrency in Go](https://www.oreilly.com/library/view/concurrency-in-go/9781491941294/)，Katherine Cox-Buday —— Go 并发唯一必读
7. [Let's Go](https://lets-go.alexedwards.net/)，Alex Edwards —— Web 开发实战
8. [Let's Go Further](https://lets-go-further.alexedwards.net/) —— 进阶 Web 开发
9. [Algorithms](https://jeffe.cs.illinois.edu/teaching/algorithms/)（Jeff Erickson）—— 免费，算法教材
10. [LeetCode 75](https://leetcode.com/studyplan/leetcode-75/) —— Go 实现 75 题

**项目验证**：
- 用 Go 写一个 RESTful API 服务器（带 middleware、路由、数据库连接、测试）
- 用 Go 写一个 CLI 工具（带 flags、subcommands、退出码）
- 用 Go 实现 5 个你熟悉的模式（比如 rate-limiter、retry-backoff 等）

**实践检验标准**：
- 能独立阅读 [Kubernetes](https://github.com/kubernetes/kubernetes) 的 controller 模式源码
- 能理解 [Prometheus](https://github.com/prometheus/prometheus) 的 tsdb 包的基本结构
- 写 1000 行 Go 代码后 review 自己，发现"这里可以用 interface 优化"

---

#### Q2（第4-6个月）：Python 深化 + 计算机网络

**学习目标**：Python 达到"能用它写系统工具"水平。理解网络协议栈。

**学习内容**：
- Python 深入（生成器、装饰器、上下文管理器、元类、描述符）
- Python 并发（threading、multiprocessing、asyncio）
- Python C 扩展基础（ctypes、cffi）
- 计算机网络（从应用层到链路层，用 Python 写协议 demo）

**核心资源**：
11. [Fluent Python](https://www.oreilly.com/library/view/fluent-python-2nd/)，Luciano Ramalho —— Python 语言深度，**必读**
12. [Python Cookbook](https://www.oreilly.com/library/view/python-cookbook-3rd/)，David Beazley —— 实战配方，**必读**
13. [Python 官方文档](https://docs.python.org/3/tutorial/) —— 最权威
14. [CPython 内部解析](https://realpython.com/products/cpython-internals-book/)
15. [Architecture Patterns with Python](https://www.cosmicpython.com/) —— DDD + TDD
16. [100 Page Python Intro](https://learnbyexample.github.io/100_page_python_intro/)，Sundeep Agarwal
17. [Computer Networking: A Top-Down Approach](https://www.amazon.com/Computer-Networking-Top-Down-Approach-7th/dp/0133594149)，Kurose & Ross
18. [Beej's Guide to Network Programming](https://beej.us/guide/bgnet/) —— 网络编程标准入门
19. [High Performance Browser Networking](https://hpbn.co/)，Ilya Grigorik —— Web 性能网络
20. [HTTP: The Definitive Guide](https://www.amazon.com/HTTP-Definitive-Guide-David-Gourley/dp/1565925092) —— HTTP 协议全面理解

**项目验证**：
- 用 Python asyncio 写一个简单的 HTTP 服务器（理解协议解析、连接管理）
- 用 Python 写一个 packet sniffer（用 scapy 或 raw socket）—— 验证你对网络层理解
- 用 ctypes 或 cffi 封装一个 C 库的 Python 接口

**实践检验标准**：
- 能读 [urllib3](https://github.com/urllib3/urllib3) 或 [aiohttp](https://github.com/aio-libs/aiohttp) 的源码
- 能解释 HTTP/1.1 和 HTTP/2 的连接复用差异及其实现细节
- 你写出的 Python 代码通过了 mypy strict 模式检查

---

#### Q3-Q4（第7-12个月）：深入计算机系统 + TypeScript 后端化

**学习目标**：理解计算机硬件-操作系统-编程语言的完整栈。TypeScript 从前端走向全栈。

**学习内容**：
- 计算机系统（位、字节、整数表示、浮点数、汇编、内存层次、缓存、异常控制流、虚拟内存、系统级 I/O、并发编程）
- 数据结构深入（用 C 理解本质——数组的内存布局、链表的 cache 行为、树的递归结构）
- TypeScript 后端（Node.js 运行时、事件循环、Stream、zlib、Crypto、Child Process、Worker Threads）

**核心资源**：
21. [Computer Systems: A Programmer's Perspective](http://csapp.cs.cmu.edu/)（CS:APP），Bryant & O'Hallaron —— **全世界最好的计算机系统书，没有之一。必读。目标：做完全部 lab**
22. CS:APP 配套实验 —— [CS:APP Lab Assignments](http://csapp.cs.cmu.edu/3e/labs.html)（Bomb Lab、Buffer Lab、Shell Lab、Malloc Lab、Proxy Lab）。**这些实验就是你的下半年计划**
23. [Deep Work](Chpters 1-4)，Cal Newport —— 读 CS:APP 需要深度工作模式
24. [Node.js 官方文档](https://nodejs.org/en/docs/) —— 不是教程，是参考
25. [Node.js Design Patterns](https://www.nodejsdesignpatterns.com/)，Mario Casciaro —— 设计模式与 Node 最佳实践
26. [Effective TypeScript](https://effectivetypescript.com/)，Dan Vanderkam —— TS 进阶
27. [TypeScript 编译器源码](https://github.com/microsoft/TypeScript) —— 了解什么是真正的类型系统
28. [深入探究 Node.js 事件循环](https://www.youtube.com/playlist?list=PLw5h0FsdC-7JIQ5WHrGvQyT7C1lMkDgX) —— Bert Belder 的演讲
29. [The Node.js Event Loop: Not So Single Threaded](https://www.youtube.com/watch?v=zphcsoSJMvM) —— 理解 libuv
30. [Node.js 源码](https://github.com/nodejs/node)

**项目验证**：
- 完成 CS:APP 的所有 lab（Bomb → Buffer → Attack → Shell → Malloc → Proxy —— 共 6 个）
- 用 TypeScript + Node.js 写一个 WebSocket 服务器（理解帧格式、握手、掩码）
- 用 Node.js 的 Worker Threads 写一个 CPU 密集型任务的并行处理系统

**实践检验标准**：
- CS:APP 学完之后，你能解释：`int x = 42;` 在内存中是什么样的？
- 你能读出反汇编，能解释为什么某些代码比另一些慢 10 倍
- 你能解释 libuv 的 event loop 实现原理（不是画图，是讲实现）

---

### 第一年总结

**可交付物**：
- 2000+ 行 Go 代码（CLI 工具 + Web 服务 + 并发程序）
- CS:APP 全部 lab 完成
- 100+ LeetCode 题全部用多种语言实现
- Python 达到系统工具编写水平
- TypeScript 从纯前端到全栈

---

## 第二年：攻占系统层

### 战略意义

"从控制抽象到底层真相。"—— 你第一年学了 Go（有 GC 的并发语言），学了 CS:APP（理解计算机系统），现在可以进入 C 和 Rust 了。

### 第二年学习日历

#### Q1-Q2（第13-18个月）：C 语言深度 + 操作系统精读

**学习目标**：C 达到"能用它写系统程序和嵌入式代码"水平。读操作系统的核心设计。

**学习内容**：
- C 语言深度（指针、数组、函数指针、存储期限、连接、预处理、宏的陷阱、setjmp/longjmp、信号、可变参数）
- C 标准库（string、stdio、stdlib、signal、setjmp、time）
- C 系统编程（进程控制、信号、IPC、管道、socket）
- 操作系统概念深化（进程和线程的实现、调度、虚拟内存、文件系统、I/O）
- x86-64 汇编阅读（不是写，是能读懂）

**核心资源**：
31. [The C Programming Language](https://www.amazon.com/Programming-Language-2nd-Brian-Kernighan/dp/0131103628)（K&R）—— **C 语言的圣经**。要做完所有习题。
32. [Advanced Programming in the UNIX Environment](https://www.amazon.com/Advanced-Programming-UNIX-Environment-3rd/dp/0321637739)（APUE）—— Unix 系统编程权威，**选读关键章节**（进程控制、信号、线程、IPC）
33. [The Linux Programming Interface](https://man7.org/tlpi/)，Michael Kerrisk —— APUE 的当代替代，**更全面**
34. [Expert C Programming: Deep C Secrets](https://www.amazon.com/Expert-Programming-Peter-Linden/dp/0131774298)，Peter van der Linden —— C 语言的冷知识和陷阱
35. [Understanding and Using C Pointers](https://www.oreilly.com/library/view/understanding-and-using/9781449378992/) —— 指针深入
36. [Operating Systems: Three Easy Pieces](https://pages.cs.wisc.edu/~remzi/OSTEP/)（OSTEP）—— **免费，操作系统入门最佳**。目标：读完全书 + 完成所有 lab 项目
37. OSTEP 项目 —— [OSTEP Projects](https://github.com/remzi-arpacidusseau/ostep-projects)（进程 run、shell、内存分配器、并发、文件系统）
38. [The Design of the UNIX Operating System](https://www.amazon.com/Design-UNIX-Operating-System-Maurice/dp/0132017997)，Maurice Bach —— 经典操作系统设计
39. [x86-64 Assembly 参考](https://cs.brown.edu/courses/cs033/docs/guides/x64_cheatsheet.pdf) —— 必备速查
40. [Modern C](https://modernc.gforge.inria.fr/)，Jens Gustedt —— C11 及以上现代写法

**项目验证**：
- 用 C 写一个简单的 shell（进程管理、管道、重定向、作业控制——经典的 CS 项目）
- 用 C 写一个内存分配器（malloc/free），理解 sbrk、free list、碎片整理——经典的 Malloc Lab
- 用 C 写一个简单的 HTTP 服务器或 WebSocket 服务器
- 用 C 实现你熟悉的 2-3 个模式（ring-buffer、free-list、arena-allocator）
- 用 OSTEP 的并发实验验证你对锁、信号量、条件变量的理解

**实践检验标准**：
- 能在30分钟内读懂一个中等复杂的 C 项目结构（如 [redis 的 networking.c](https://github.com/redis/redis/blob/unstable/src/networking.c)）
- 能解释 `valgrind` 或 AddressSanitizer 的原理
- 能解释虚拟内存到物理内存的转换过程（页表、TLB、缺页中断）
- 理解 / 能辨析堆栈内存分配的区别：`int arr[100]` 和 `int* arr = malloc(100 * sizeof(int))` 的区别（不仅是语法，是它们分配的实际位置和生存期）

---

#### Q3-Q4（第19-24个月）：Rust 入门 + 数据库内核

**学习目标**：Rust 达到"能读源码、能写小工具"水平。理解数据库存储引擎核心。

**学习内容**：
- Rust 基础（所有权、借用、生命周期、模式匹配、trait、泛型、闭包、迭代器）
- Rust 进阶（unsafe、FFI、Pin、Future、async/await、Send/Sync）
- Rust 工具链（Cargo、clippy、rustfmt、cargo doc、cargo test、criterion bench）
- 数据库基础（存储引擎、B-Tree、LSM-Tree、事务、ACID、MVCC）

**核心资源**：
41. [The Rust Programming Language](https://doc.rust-lang.org/book/) —— Rust Book，从头到尾，**所有习题必做**
42. [Rust by Example](https://doc.rust-lang.org/stable/rust-by-example/) —— 代码入门
43. [Programming Rust](https://www.oreilly.com/library/view/programming-rust-2nd/)，Jim Blandy & Jason Orendorff —— 官方第二权威书
44. [Rustonomicon](https://doc.rust-lang.org/nomicon/) —— unsafe Rust 唯一指南（不是你今年要深入，但要读一遍）
45. [Rust Design Patterns](https://rust-unofficial.github.io/patterns/) —— 与你的知识体系高度契合
46. [Learn Rust With Entirely Too Many Linked Lists](https://rust-unofficial.github.io/too-many-lists/) —— Rust 所有权和借用系统的终极练习
47. [Rust Atomics and Locks](https://marabos.nl/atomics/)，Mara Bos —— Rust 并发深入
48. [Command Line Rust](https://www.oreilly.com/library/view/command-line-rust/9781098109424/) —— Rust CLI 实战
49. [Zero To Production In Rust](https://www.zero2prod.com/) —— Rust 后端开发
50. [Designing Data-Intensive Applications](https://dataintensive.net/)（DDIA），Martin Kleppmann —— **分布式系统和存储的权威书。必读。**
51. [Database Internals](https://www.oreilly.com/library/view/database-internals/9781492040330/)，Alex Petrov —— 存储引擎深入
52. [PostgreSQL 源码](https://github.com/postgres/postgres) —— 存储部分
53. [SQLite 源码](https://github.com/sqlite/sqlite) —— B-Tree 实现的极佳参考
54. [LevelDB 源码](https://github.com/google/leveldb) —— LSM-Tree 的经典实现
55. [Redis 源码](https://github.com/redis/redis) —— 事件驱动、内存存储

**项目验证**：
- 用 Rust 写一个 CLI 工具（理解 Cargo、crate、error handling、testing）
- 用 Rust 实现一个简单的键值存储引擎（参考小小 LevelDB，理解 LSM-Tree、SSTable、compaction）
- 用 Rust FFI 调用你之前写的 C 库（理解 Rust 和 C 的交互）
- 用 Rust 写一个并发的 TCP echo 服务器（理解 async/await 和线程池的两种方式）

**实践检验标准**：
- 能读懂 [tokio](https://github.com/tokio-rs/tokio) 的基本 reactor 模式
- 能用 Rust 正确实现链表（知道这是所有权系统的经典挑战）
- 能解释 B-Tree 和 LSM-Tree 的读写放大差异及其适用场景

---

### 第二年总结

**可交付物**：
- K&R 习题全做 + APUE/OSTEP 关键章节
- 用 C 写出 shell、内存分配器、HTTP 服务器
- 用 Rust 写出 CLI 工具 + 键值存储引擎
- 读完 DDI 的存储和复制部分
- Rust Book 习题全做

---

## 第三年：双线作战

### 战略意义

"从学习者到实践者。"前两年你学了语言和系统知识，第三年开始把它们用起来。同时深入 TypeScript 的编译器层面和 Web 工程架构。

### 第三年学习日历

#### Q1-Q2（第25-30个月）：Rust 深化 + 编译原理

**学习目标**：Rust 达到生产级水平。理解编译器工作方式。

**学习内容**：
- Rust 深入（unsafe、FFI、proc macro、Pin、async/await 实现细节、Pin 的语义）
- Rust 生态重点库（tokio、axum/actix、serde、clap、tracing、reqwest）
- 编译原理基础（词法分析、语法分析、语义分析、中间代码生成、目标代码生成）
- 重点：用 Rust 写一个简单的编译器/解释器

**核心资源**：
56. [The Rust Standard Library 源码](https://github.com/rust-lang/rust/tree/master/library/std) —— 最终权威
57. [Rust 编译器源码](https://github.com/rust-lang/rust) —— 特别是 rustc 和 rust-analyzer
58. [The Little Book of Rust Macros](https://veykril.github.io/tlborm/) —— Rust 宏权威
59. [Compilers: Principles, Techniques, and Tools](https://www.amazon.com/Compilers-Principles-Techniques-Tools-2nd/dp/0321486811)（Dragon Book）—— 编译原理权威
60. [Crafting Interpreters](https://craftinginterpreters.com/)，Bob Nystrom —— **最好的手写解释器教材，免费在线。必做所有练习**
61. [Write A Compiler In Go / Rust](https://compilerbook.com/)，Thorsten Ball —— 手写编译器（Rust 版）
62. [Writing an Interpreter in Rust](https://github.com/rust-hosted-langs/book) —— Rust 版本
63. [LLVM 源码](https://github.com/llvm/llvm-project) —— 了解 LLVM IR 和优化 pass
64. [Structure and Interpretation of Computer Programs](https://mitpress.mit.edu/sites/default/files/sicp/index.html)（SICP）—— 编程思维的最终修炼

**项目验证**：
- 用 Rust 写一个简单的 Lisp/JS/Python 子集解释器（Crafting Interpreters 的 jlox 或 clox）
- 或者实现一个小的玩具语言并编译到 LLVM IR
- 对比 Rust/Go 在生产中的性能差异（做一个简单的推理或IO密集型任务benchmark）

**实践检验标准**：
- 能读懂 [rustc](https://github.com/rust-lang/rust) 编译器的部分源码
- 能解释 Rust 的 trait 是如何编译成 vtable 调用的
- 能解释编译器优化（常量折叠、死代码消除、内联扩展）
- 了解LLVM三层架构（前端、IR、后端）

---

#### Q3-Q4（第31-36个月）：TypeScript 工程架构 + 分布式系统

**学习目标**：TypeScript 从"会写"到"会设计"（大工程架构）。理解分布式系统的核心问题及解决方案。

**学习内容**：
- TypeScript 深入（条件类型、映射类型、模板字面量类型、递归类型、类型体操——type-challenges 上刷题）
- TypeScript 编译器 API（TS AST、Transformer、Custom Plugin）
- 前端框架源码（React 的核心 reconciler 和 fiber 架构 / Vue 3 的 reactivity 和 compiler）
- Node.js 运行时深入（V8 内存模型、libuv、C++ addon）
- 分布式系统核心（一致性、共识算法、分区、复制、故障检测、CAP）
- 用 Go/Rust 实现分布式系统组件

**核心资源**：
65. [TypeScript 官方文档：TypeScript Compiler API](https://github.com/microsoft/TypeScript/wiki/Using-the-Compiler-API)
66. [Type Challenges](https://github.com/type-challenges/type-challenges) —— TypeScript 类型体操
67. [React 源码设计](https://github.com/facebook/react) —— 特别是 react-reconciler 包
68. [Vue.js 3 源码](https://github.com/vuejs/core) —— 深入 reactivity 和 compiler
69. [Inside V8](https://v8.dev/) —— V8 官方博客
70. [V8 源码](https://github.com/v8/v8) —— 了解 JS 引擎如何执行你的代码
71. [Distributed Systems](https://www.distributed-systems.net/index.php/books/ds3/)，Maarten van Steen & Andrew Tanenbaum
72. [Distributed Systems for Fun and Profit](https://book.mixu.net/distsys/)，Mika —— 免费，精炼
73. [MIT 6.824: Distributed Systems](https://pdos.csail.mit.edu/6.824/) —— **分布式系统最好的课**，含 lab（Raft KV、Sharded KV、Fault-tolerant MapReduce）
74. [DDIA](https://dataintensive.net/)—— 第5章（复制）、第6章（分区）、第7章（事务）、第8章（分布式系统的麻烦）、第9章（一致性与共识）——**精读**
75. [etcd 源码](https://github.com/etcd-io/etcd) —— Raft 共识算法的一个标准 Go 实现
76. [ZooKeeper 论文](https://www.usenix.org/legacy/event/atc10/tech/full_papers/Hunt.pdf) —— Zab 共识协议
77. [Raft 论文](https://raft.github.io/raft.pdf) —— 共识算法论文
78. [Gossip 协议论文](https://www.cs.cornell.edu/courses/cs6410/2018fa/slides/18-gossip.pdf) —— 最终一致性基础
79. [The Google File System](https://static.googleusercontent.com/media/research.google.com/en//archive/gfs-sosp2003.pdf)
80. [MapReduce](https://static.googleusercontent.com/media/research.google.com/en//archive/mapreduce-osdi04.pdf)
81. [Bigtable](https://research.google/pubs/pub27898/)
82. [Dynamo: Amazon's Highly Available Key-value Store](https://www.allthingsdistributed.com/files/amazon-dynamo-sosp2007.pdf)
83. [Kafka: A Distributed Messaging System for Log Processing](https://notes.stephenholiday.com/Kafka.pdf)

**项目验证**：
- 用 TypeScript 写一个「类型安全的」GraphQL 或 tRPC 服务——重点不在业务，类型基础设施层设计与工程架构
- 用 Go 实现 Raft 共识算法的一个组件（参考 MIT 6.824 lab）
- 用 Rust 或 Python 写一个 WebSocket 负载均衡器
- 实现一个简单但是类型安全的分布式键值存储（基于 Raft 共识）

**实践检验标准**：
- 能读懂 React reconciler 或 Vue reactivity 的核心源码
- 能解释 Raft 的 Leader Election 和 Log Replication
- 能解释 CAP 理论和 PACELC 权衡
- 能解释 ZooKeeper 的 ZAB 和 Raft 的异同

---

## 第四年：开源主力贡献

### 战略意义

"从消费者到生产者。"你前三年的积累都是为了这一年——给核心开源项目做出有意义的贡献。

### 选择贡献方向

根据你的技术栈优势（TypeScript + Go + Rust + C + Python），以下是你的潜在贡献方向：

| 领域 | 项目 | 入口 |
|------|------|------|
| 云基础设施（Go） | [Kubernetes](https://github.com/kubernetes/kubernetes) | good-first-issue + sig-contributor-experience |
| 云基础设施（Go） | [Prometheus](https://github.com/prometheus/prometheus) | 存储引擎、PromQL |
| 云基础设施（Go） | [etcd](https://github.com/etcd-io/etcd) | Raft、存储 |
| 云基础设施（Go） | [Docker/Moby](https://github.com/moby/moby) | 容器运行时 |
| 系统编程（Rust/C） | [rust-lang/rust](https://github.com/rust-lang/rust) | 编译器、标准库 |
| 系统编程（Rust/C） | [Tokio](https://github.com/tokio-rs/tokio) | async runtime |
| 系统编程（Rust/C） | [Redis](https://github.com/redis/redis) | 存储、网络 |
| 系统编程（Rust/C） | [PostgreSQL](https://github.com/postgres/postgres) | 存储引擎 |
| 前端/工具（TS） | [TypeScript](https://github.com/microsoft/TypeScript) | 编译器 |
| 前端/工具（TS） | [Vite](https://github.com/vitejs/vite) | 构建工具 |
| 前端/工具（TS） | [ESLint](https://github.com/eslint/eslint) | Lint 规则 |
| 前端/工具（TS） | [pnpm](https://github.com/pnpm/pnpm) | 包管理器 |
| 数据库（Rust） | [RisingWave](https://github.com/risingwavelabs/risingwave) | 流式数据库 |
| 数据库（Rust） | [GreptimeDB](https://github.com/GreptimeTeam/greptimedb) | 时序数据库 |

### 贡献路线

#### Q1-Q2（第37-42个月）：建立贡献习惯

1. **选一个项目** —— 选你日常使用且最感兴趣的一个。不贪多。
2. **修文档** —— 从修错别字、改进文档开始，理解项目的贡献流程
3. **写测试** —— 测试是最容易的代码贡献，同时让你深入理解功能
4. **修 bug** —— 从 labeled "good first issue" 或 "help wanted" 开始

**原则**：
- 不要同时贡献多个项目。**一年只深耕一个项目**。
- 每个 PR 都要做到：代码质量好、注释清晰、测试覆盖、commit message 规范
- 回复 review 意见要耐心，每个回复都附上修改 commit

#### Q3-Q4（第43-48个月）：深度贡献

- 在你选择的项目中找到你擅长的领域（比如你有 Go 经验和分布式系统知识，就做存储/调度相关）
- 主导一个 feature 的实现
- 参加社区会议、code review 他人代码
- 成为该领域的"领域专家"（你认识 10+ 核心 contributor，他们认识你）

### 开源贡献的核心资源

84. [How to Contribute to Open Source](https://opensource.guide/how-to-contribute/) —— GitHub 官方指南
85. [First Timers Only](https://www.firsttimersonly.com/) —— 新手友好的 issue
86. [Good First Issues](https://goodfirstissue.dev/) —— 多语言多项目过滤
87. [Up For Grabs](https://up-for-grabs.net/) —— 寻找 issue
88. [CNCF Contributor Guide](https://contribute.cncf.io/) —— 云原生贡献指南
89. [Kubernetes Contributor Guide](https://www.kubernetes.dev/docs/guide/) —— K8s 贡献流程
90. [Rust Contributor Guide](https://rustc-dev-guide.rust-lang.org/) —— Rustc 贡献流程
91. [This Week in Rust](https://this-week-in-rust.org/) —— 每周关注 Rust 生态
92. [KubeWeekly](https://kubeweekly.io/) —— 每周关注 K8s 生态
93. [Producing Open Source Software](https://producingoss.com/)，Karl Fogel —— 开源项目管理

---

## 第五年：商业化探索

### 战略意义

"从技术专家到价值创造者。"前四年你建立了深厚的技术积累，第五年目标是让你的知识产生实际价值。

### 三条变现路径

#### 路径 A：知识产品（最快启动，第5年目标 $500-2000/月）

基于你的技术深度（6 语言 + 系统知识），你可以做以下内容：

| 产品形式 | 内容 | 平台 |
|---------|------|------|
| 技术博客/Newsletter | "6 种语言看编程"系列 | Substack / 公众号 |
| 技术课程 | "从 Go 到 Rust：系统编程的两种哲学" | Udemy / Gumroad |
| 电子书 | 经过验证后的《6种语言对比系统编程》《从Rust入门到精通》 | Leanpub / 电子书 |
| 咨询 | "从前端到全栈系统工程师转型" 一对一 | Clarity / 个人网站 |

**成功前提**：你的技术博客/社交媒体在第 3-4 年就要开始建立，到第 5 年才有足够读者。

#### 路径 B：SaaS 工具（更大潜力，第5年目标 $2000-5000/月）

基于你的系统知识构建工具：

| 产品想法 | 技术栈 | 市场验证 |
|---------|------|---------|
| 代码审查辅助工具（跨多种语言的自动化检评） | TypeScript + Rust | 企业开发团队 |
| 存储引擎/数据库性能诊断工具 | Rust + C + Go | DBA、SRE |
| 多语言技术项目的架构分析SaaS | TypeScript + Go | 技术管理者 |

**成功前提**：找到切实的、刚需的痛点，用小范围 MVP 验证（你所在的团队日常有什么痛点，看看市面上是否已经有稳定的可替代方案）。

#### 路径 C：Founding Engineer / 技术合伙人（更高上限）

- 加入一个早期创业公司做第 1-5 号工程师
- 如果你在 5 年内建立了足够的技术影响力、开源项目经历和产品思维，可以找创始人合作或自己从 side project 孵化
- 这要求你在前 4 年就**持续在个人 side project 或开源社区中有输出、发声和积累**

### 财务独立的核心原则

94. [The Mom Test](https://www.momtestbook.com/)，Rob Fitzpatrick —— **在写任何代码前先读这本书**。如何验证需求。
95. [Start Small, Stay Small](https://startupbook.net/)，Rob Walling —— 独立开发圣经
96. [Indie Hackers](https://www.indiehackers.com/) —— 独立开发者社区，看别人如何做
97. [levels.io](https://levels.io/) —— Pieter Levels，独立开发的代表
98. [Nadia Eghbal, *Working in Public*](https://www.amazon.com/Working-Public-Making-Maintenance-Software/dp/0578675862) —— 开源经济的全景分析
99. [GitHub Sponsors](https://github.com/sponsors) —— 开源赞助
100. [Polar.sh](https://polar.sh/) —— 开源商业化新平台

---

## 第四到第五年的补充：经典论文必读清单

这些是计算机科学最核心的论文。建议在第 4-5 年系统性地读完。

### 分布式系统核心论文

101. [The Byzantine Generals Problem](https://lamport.azurewebsites.net/pubs/byz.pdf)，Lamport, Shostak & Pease —— 拜占庭容错的开端。
102. [Time, Clocks, and the Ordering of Events in a Distributed System](https://lamport.azurewebsites.net/pubs/time-clocks.pdf)，Lamport —— 逻辑时钟、分布式系统中的事件排序。
103. [Impossibility of Distributed Consensus with One Faulty Process](https://groups.csail.mit.edu/tds/papers/Lynch/jacm85.pdf)（FLP Impossibility）—— 分布式共识的理论局限。
104. [The Chubby Lock Service for Loosely-Coupled Distributed Systems](https://static.googleusercontent.com/media/research.google.com/en//archive/chubby-osdi06.pdf) —— Google 的分布式锁服务。
105. [Paxos Made Simple](https://lamport.azurewebsites.net/pubs/paxos-simple.pdf)，Lamport —— 共识算法。
106. [In Search of an Understandable Consensus Algorithm](https://raft.github.io/raft.pdf)（Raft 论文）—— Raft 共识协议
107. [ZooKeeper: Wait-free coordination for Internet-scale systems](https://www.usenix.org/legacy/event/atc10/tech/full_papers/Hunt.pdf)
108. [Dynamo: Amazon's Highly Available Key-value Store](https://www.allthingsdistributed.com/files/amazon-dynamo-sosp2007.pdf)
109. [Bigtable: A Distributed Storage System for Structured Data](https://research.google/pubs/pub27898/)
110. [Spanner: Google's Globally-Distributed Database](https://research.google/pubs/pub39966/)
111. [The Google File System](https://static.googleusercontent.com/media/research.google.com/en//archive/gfs-sosp2003.pdf)
112. [MapReduce: Simplified Data Processing on Large Clusters](https://static.googleusercontent.com/media/research.google.com/en//archive/mapreduce-osdi04.pdf)
113. [Dapper, a Large-Scale Distributed Systems Tracing Infrastructure](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/36356.pdf) —— 分布式追踪的起源。

### 操作系统和网络核心

114. [End-to-End Arguments in System Design](https://web.mit.edu/Saltzer/www/publications/endtoend/endtoend.pdf)，Saltzer, Reed & Clark —— 系统设计的核心原则。
115. [The Dynamics of Caching](https://www.usenix.org/legacy/publications/library/proceedings/osdi00/technical_papers/fan/fan.pdf)
116. [A Note on Distributed Computing](https://scholar.harvard.edu/files/waldo/files/waldo-1994.pdf)
117. [The Structure of the 'THE'-Multiprogramming System](https://www.cs.utexas.edu/users/EWD/ewd01xx/EWD196.PDF)，Dijkstra —— 操作系统结构设计的经典。

### 编程语言和编译

118. [Reflections on Trusting Trust](https://www.cs.cmu.edu/~rdriley/487/papers/Thompson_1984_ReflectionsonTrustingTrust.pdf)，Ken Thompson —— 编译器后门的思想实验。
119. [Go To Statement Considered Harmful](https://homepages.cwi.nl/~storm/teaching/reader/Dijkstra68.pdf)，Dijkstra —— 结构化编程。
120. [On the Criteria to Be Used in Decomposing Systems into Modules](https://www.win.tue.nl/~wstomv/edu/2ip30/references/parnas_criteria_decomposing.pdf)，Parnas —— 模块化设计原则。
121. [Monitors: An Operating System Structuring Concept](https://www.microsoft.com/en-us/research/uploads/prod/2020/12/hoare-monitors.pdf)，Hoare —— 并发编程模型。

---

## 学习习惯与策略总纲

### 每周时间分配

| 活动 | 小时（平时） | 小时（周末） | 每天频率 |
|------|------------|------------|---------|
| 阅读 + 学新内容 | 1 小时 | 3小时 | 阅读加实践 |
| 编码实践 | 1 小时 | 3小时 | 每天写一些 |
| 源码阅读 | 0.5 小时 | 1小时 | 周末可以多读，工作日穿插 |
| 写笔记/博客/记录 | 0.5 小时 | 1小时 | 输出驱动力 |
| **合计** | **3 小时/工作日** | **8小时/周末日** | **约31小时/周** |

你工作日有本职工作，不是全职学生。每天保证至少 1.5 小时有效学习时间，周末 5-6 小时。每周合理可做到 20 小时，足够坚持。

### 用"福格行为模型"建立习惯

- **动机**——你的"我想学计算机的一切"就是最强的内驱力
- **能力**——从每天 0.5 小时开始，不要一开始就定 3 小时
- **触发**——每天固定时间（建议晚上 9-11 点），设置手机提醒

### 检验和学习循环

每季度自评一次：

1. 过去 90 天我产出了什么？（代码、文章、PR、项目）
2. 我学到了什么新概念？能否用 Feynman 方法（用自己的话解释给小白听懂）讲给别人听？
3. 我下一步要解决什么问题？
4. 如果过去 90 天没有显著进步——分析原因：是方向错了还是时间不够？

### 元资源（学习方法论）

122. [Teach Yourself Programming in Ten Years](https://norvig.com/21-days.html)，Peter Norvig —— **起点**
123. [Peak: Secrets from the New Science of Expertise](https://www.amazon.com/Peak-Secrets-New-Science-Expertise/dp/0544947223)，Ericsson —— 刻意练习的权威
124. [《The Art of Learning》](https://www.joshwaitzkin.com/the-art-of-learning)，Josh Waitzkin —— 象棋冠军转太极冠军，元学习
125. [《Deep Work》](https://www.calnewport.com/books/deep-work/)，Cal Newport —— 深度工作的科学
126. [《Atomic Habits》](https://jamesclear.com/atomic-habits)，James Clear —— 习惯养成
127. [《So Good They Can't Ignore You》](https://www.amazon.com/So-Good-They-Cant-Ignore-You/dp/1455509124)，Cal Newport —— 技能积累 vs 热情
128. [《The Pragmatic Programmer》](https://pragprog.com/titles/tpp20/)，Andy Hunt & Dave Thomas —— 编程界的经典
129. [MIT Missing Semester](https://missing.csail.mit.edu/) —— 开发的实用工具技能
130. [Stanford CS 106系列](https://cs.stanford.edu/bachelors/cs-bs)
131. [OSSU Computer Science](https://github.com/ossu/computer-science) —— 开源 CS 学位
132. [CS自学指南](https://csdiy.wiki/) —— 国内同学整理的CS自学路线

---

## 你的实战项目清单（5年，按语言和领域）

### 必须做的核心项目（含精读的书和相关源代码）

| 项目 | 语言 | 时间 | 说明 |
|------|------|------|------|
| CS:APP 全部 Lab | C | 第一年 | 计算机系统理解 |
| OSTEP 全部项目 | C | 第二年 | 操作系统理解 |
| Shell 实现 | C | 第二年 | 进程、管道、信号 |
| Malloc 实现 | C | 第二年 | 内存分配器 |
| HTTP 服务器 | C | 第二年 | 网络协议实现 |
| Raft KV 存储 | Go | 第二~三年 | 分布式共识 |
| Lisp/JS解释器 | Rust | 第三年 | 编译原理 |
| 键值存储引擎 | Rust | 第三年 | LSM-Tree |
| MIT 6.824 Lab | Go | 第三年 | 分布式系统 |
| type-challenges | TS | 第三年 | TypeScript类型系统 |
| 主导开源 Feature | 按需 | 第四年 | 社区贡献 |
| Side Project 产品 | 按需 | 第五年 | 商业化 |

---

## 检验标准总表

| 年份 | 语言掌握（按层） | 项目产出 | 开源贡献 | 财务指标 |
|------|----------------|---------|---------|---------|
| 第1年 | TS/Go/Python 第二层、C 第一层 | 2-3 个 CLI + CS:APP Lab + OSTEP项目 | 开始提出 Issue（非 PR） | 维持本职 |
| 第2年 | C 第三层、Rust 第二层、Go 第三层 | Shell+Malloc+KV store+解释器 | 1-3 个小 PR | 维持本职 |
| 第3年 | Rust/TS 第三层、全部六语言第二层 | MIT 6.824 Lab、生产级工具 | 5-10 个 PR | 微量 Sponsor |
| 第4年 | 2-3 语言第四层 | 主导开源 Feature | 成体系参与、自身项目 200+ star | $0-500/月 |
| 第5年 | 2-3 语言第四层以上 | 独立产品 MVP | 成为领域 maintainer | $500-5000/月 |

---

## 第零条：从今天开始

你需要买的：
- 一个用于建立技术博客的域名（用 GitHub Pages 或 Cloudflare Pages 搭载你本来的仓库，可参考之前我们写的自定义域名迁移计划）
- 给 Go/Rust/C 的编程环境 —— 你已经有了（只要装好 cargo、gcc、go）
- 一本作业本（或 notion 文档）—— 记录每天学了什么

你不需要买的：
- **课程**（除非你想加速某些方向，比如 Udemy 上的 Go 课程在打折时可以买——但不是必须的）
- **证书**（在技术领域，作品比证书重要 100 倍）
- **新电脑**（你已经有了）

> "做好一件事，就等于做好了所有事。"  
> —— 这个五年计划最重要的原则：每个阶段只做一件事，不要同时做两件事。在你没把 Go 学到第二层之前，不要碰 Rust。在你没把 C 学到第三层之前，不要试图理解 Rust 的所有权。顺序决定成败。

---

这个计划的全部核心是 **5 步走**，每步大约 1 年，总计 5 年专注于计算机基础。建议把它保存好，每季度拿出来对照一下，看看进度是否符合预期。当然，**计划是死的，人是活的**，根据实际的工作节奏、职场变动、家庭因素可以动态调整半年时间，不要硬套节奏导致 burnout。
