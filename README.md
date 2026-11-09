### Hi, I'm TokaiTeio666 👋

**后端工程 / AI Infra** · 华南师范大学 (SCNU)

> Undergraduate at SCNU, focused on backend engineering and AI infrastructure.
> I care about LLM serving, agent memory & retrieval, and performance numbers that actually reproduce.

- 🔭 最近在做 **LLM 服务化**：网关的准入控制、限流、熔断、降级与缓存，以及 TTFT / TPOT 压测
- 🧠 同时在研究 **Agent 长期记忆的向量检索 I/O 优化**：磁盘常驻 Vamana + PQ，内存预算受限下的 Top-K ANN
- 🧱 工程偏好：可复现的实验、真实的故障路径、上线可查的指标
- 📫 联系我：**teiocurry@gmail.com**

---

## 精选项目 / Featured

| 项目 | 简介与亮点 |
| --- | --- |
| **[llm-serving-lab](https://github.com/TokaiTeio666/llm-serving-lab)**<br/><sub>Python · FastAPI · Docker</sub> | LLM 网关 + 可注入故障的模型服务 + TTFT/TPOT 压测工具。实现按租户限流、准入控制、熔断、重试降级、精确匹配缓存与 SSE 流式错误事件；对接真实 vLLM（Qwen2.5-1.5B 主模型 + 0.5B 降级模型），附 Prometheus 与 13 面板 Grafana。 |
| **[agent-aware](https://github.com/TokaiTeio666/agent-aware)**<br/><sub>C++ · Vamana · PQ</sub> | 面向 Agent 长期记忆的磁盘向量检索 I/O 优化原型（OS 大赛参赛作品）。100k×128 合成数据集上 Recall@10 **0.877**、平均延迟 **1.14 ms**、单线程 **878 QPS**；含 WAL / SSTable 动态写入路径与可复现实验口径。 |
| **[ZSLIB-Newspaper-Archiver](https://github.com/TokaiTeio666/ZSLIB-Newspaper-Archiver)**<br/><sub>Python · Selenium · Pillow</sub> | 数字图书馆历史报纸批量采集与归档。自动翻页、按原图比例高清裁剪、解析报刊名/日期/版次并生成标准化 Word 文档。 |
| **[pixeltown](https://github.com/TokaiTeio666/pixeltown)**<br/><sub>Python · 桌面悬浮窗</sub> | 漂在桌面上的像素小镇：世界自动演进，支持鼠标穿透、窗口位置记忆与优雅退出存档。 |

## 技术栈 / Tech Stack

![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

## 其他项目 / More

- **[Genshin_Server_Switcher](https://github.com/TokaiTeio666/Genshin_Server_Switcher)** — 原神官服 / B 服一键切换，改 `config.ini` 复用同一套游戏资源（Windows 批处理）
- **[surf](https://github.com/TokaiTeio666/surf)** — 仿 Edge 离线冲浪小游戏（数据结构课程作业）

---

<sub>项目里的实验数据、复现命令与口径都写在各自仓库的 README 中。</sub>
