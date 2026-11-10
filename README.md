### Hi, I'm TokaiTeio666 👋

**Java 后端 · Agent 开发 · 2028 届** · 华南师范大学 (211 / 双一流) · 软件工程

> 后端 + Agent 方向在读本科生，关注高并发系统、缓存一致性与 LLM 应用的服务端工程化。
> Backend + agent engineer in training, focused on high-concurrency systems, cache consistency and production-grade LLM applications.
>
> 正在寻找 **Java 后端 / Agent 开发实习（2027 暑期 / 日常）**。

- 🎯 求职意向：Java 后端 / Agent 开发实习
- 🔧 主力技术栈：Java / Spring Boot / MySQL / Redis / Kafka / Docker
- 🧠 Agent 开发：LLM 网关治理、异步 Agent 平台、混合检索与长期记忆
- 🏆 中国机器人及人工智能大赛 全国三等奖 / 广东省一等奖 · 全国大学生数学建模竞赛 广东省一等奖
- 🧱 工程偏好：可复现的压测、真实的故障路径、上线可查的指标
- 📫 联系我：**teiocurry@gmail.com**

---

## 精选项目 / Featured

| 项目 | 简介与亮点 |
| --- | --- |
| **[sun-life](https://github.com/TokaiTeio666/sun_life)**<br/><sub>Java 17 · Spring Boot 3 · MySQL 8 · Redis 7 · Kafka · Redisson</sub> | 本地生活点评平台后端（仿大众点评）。**布隆过滤器**（Redis BitMap）+ 空值缓存挡穿透，互斥锁/逻辑过期防击穿，TTL ±10% 抖动防雪崩；秒杀链路用 Lua 原子扣减 + **Kafka 异步下单**（`acks=all` + 幂等生产者、手动提交 offset、重试 3 次进 DLT），200/500/1000 并发实测 **9,600~10,000 QPS**、1000 并发 P99 **117ms**，**零超卖、零重复下单**；点赞 BitMap 相比 ZSet 内存降至约 **1/500**，日 UV 用 HyperLogLog。压测脚本与完整数据见 [perf/README.md](https://github.com/TokaiTeio666/sun_life/blob/master/perf/README.md)。<br/><sub><i>Dianping-style local-life backend with a Bloom filter, BitMap likes, HyperLogLog UV and Kafka-based async seckill — ~10k QPS at 1,000 concurrency with zero oversell.</i></sub> |
| **[codepilot-agent](https://github.com/TokaiTeio666/codepilot-agent)**<br/><sub>Python · FastAPI · LangGraph · Redis · Docker</sub> | 异步 AI 编程 Agent 平台（Open SWE 二次开发）。GitHub App 三层凭据（JWT → installation token → 按仓库收紧权限），webhook 做 HMAC-SHA256 验签与 delivery 幂等；事件进 Redis Stream 后由消费者组在全局并发上限内消费，失败指数退避、超限进死信；Agent 在独立沙箱改码、跑测试并回写 draft PR。完整链路（含失败矩阵与 Redis key）见 [docs/GITHUB_PIPELINE.md](https://github.com/TokaiTeio666/codepilot-agent/blob/main/docs/GITHUB_PIPELINE.md)。<br/><sub><i>Async AI coding agent on Open SWE: GitHub App auth, HMAC-verified webhooks, Redis Stream ingress with retry/DLQ, sandboxed edits and draft-PR writeback.</i></sub> |
| **[mylife](https://github.com/TokaiTeio666/mylife)**<br/><sub>FastAPI · Next.js · PostgreSQL · pgvector</sub> | 多用户个人知识库 SaaS。Obsidian ZIP / Git 导入，jieba + tsvector + pgvector 三路 RRF 混合检索，带引用流式对话与提示注入防护；日/月/年复盘由 LLM 语义抽取 + 确定性 G0–G9 门禁把关；多租户 FORCE RLS。<br/><sub><i>Multi-tenant personal knowledge-base SaaS with hybrid lexical + vector retrieval (RRF), cited streaming chat and tenant-level row security.</i></sub> |
| **[llm-serving-lab](https://github.com/TokaiTeio666/llm-serving-lab)**<br/><sub>Python · FastAPI · Docker · Prometheus</sub> | LLM 网关 + 可注入故障的模型服务 + TTFT/TPOT 压测工具。实现租户级限流、准入控制、熔断、重试降级、精确匹配缓存与 SSE 流式错误事件；对接真实 vLLM（Qwen2.5-1.5B 主模型 + 0.5B 降级模型），附 Prometheus 与 13 面板 Grafana。<br/><sub><i>LLM gateway with rate limiting, admission control, circuit breaking and caching, plus a fault-injectable vLLM backend and TTFT/TPOT benchmark harness.</i></sub> |
| **[agent-aware](https://github.com/TokaiTeio666/agent-aware)**<br/><sub>C++ · Vamana · PQ</sub> | 面向 Agent 长期记忆的磁盘向量检索 I/O 优化原型（OS 大赛参赛作品）。100k×128 数据上 Recall@10 **0.877**、平均延迟 **1.14ms**、单线程 **878 QPS**；实现 WAL / SSTable 写入路径，附可复现实验脚本与数据口径。<br/><sub><i>Disk-resident Vamana + PQ index for agent long-term memory: 0.877 Recall@10 at 1.14 ms and 878 QPS single-threaded.</i></sub> |
| **[SemaLink](https://github.com/TokaiTeio666/SemaLink)**<br/><sub>ArkTS · HarmonyOS · DSK/SoftBus</sub> | HarmonyOS 多设备语义通信中间件：设备语义路由选出最可能持有答案的设备，按 L0–L3 分级获取证据，用任务充分性反馈（ENOUGH / NEED_MORE / ABORT）决定何时停止传输。双真机已验证 DSK/SoftBus 通道与 QUERY / ACK / RESULT 全链路。<br/><sub><i>HarmonyOS multi-device semantic-communication middleware with device routing, tiered evidence transfer and task-sufficiency feedback.</i></sub> |

## 技术栈 / Tech Stack

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![JMeter](https://img.shields.io/badge/JMeter-D22128?style=flat-square&logo=apachejmeter&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

<sub>Agent / AI 方向：Python · FastAPI · PostgreSQL / pgvector · vLLM · LangGraph · C++</sub>

## 其他项目 / More

- **[Genshin_Server_Switcher](https://github.com/TokaiTeio666/Genshin_Server_Switcher)** — 原神官服 / B 服一键切换，改 `config.ini` 复用同一套游戏资源（Windows 批处理）
- **[surf](https://github.com/TokaiTeio666/surf)** — 仿 Edge 离线冲浪小游戏（数据结构课程作业）
- **[ZSLIB-Newspaper-Archiver](https://github.com/TokaiTeio666/ZSLIB-Newspaper-Archiver)** — 数字图书馆历史报纸批量采集与归档：自动翻页、按原图比例高清裁剪、解析报刊名/日期/版次并生成 Word 文档（Python · Selenium · Pillow）
- **[pixeltown](https://github.com/TokaiTeio666/pixeltown)** — 漂在桌面上的像素小镇：世界自动演进，支持鼠标穿透、窗口位置记忆与优雅退出存档（Python · 桌面悬浮窗）

---

<sub>实验数据、复现命令与口径写在各自仓库的 README 中。</sub>
