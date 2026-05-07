# V2 Changelog (相对 V1)

V1 创建于 2026-03-13、最后更新 2026-04-26。
V2 创建于 2026-05-07，基于系统调研 + Codex 独立审查。

## 新增（Phase 层级）

### Phase 0：2026 视频生成全景
插入位置：在原 `#overview`（架构组件全景）之前。

- **闭源商业基线**：Sora 2、Kling 3.0、Veo 3.1、Wan 2.5/2.6/2.7（仅 API）、Runway Gen-4 / 4.5、Seedance / Doubao Video。仅作能力参考，不学内部架构。
- **开源主力**：HunyuanVideo 1.5、Wan 2.2、LTX-2.3、Open-Sora 2.0、Helios、NVIDIA Cosmos 2.5。

### Phase 1.5：Flow Matching 一周冲刺
插入位置：Phase 1 之后、Phase 2 之前。

- 主教材：MIT 6.S184 (2026 IAP)（替代 HF Diffusion Course 作为主教材）
- 补充：arXiv 2506.02070、Lipman 2023 FM 论文、SD3、Diffusion Meets Flow Matching
- 动手：Lab 1 toy → CIFAR-10 上对比 DDPM vs FM 训练曲线

### Phase 3.5：自回归扩散与实时生成
插入位置：Phase 3 之后、Phase 4 之前。

- 论文链：CausVid → Causal Forcing → Helios + DyDiT++ + TMLR'25 综述
- 动手：跑 Helios 蒸馏版 inference（6GB 显存即可） + 写 1500 字演进笔记
- 定位：**read + run + 写笔记**，不是训练复现（H100 集群级目标，不适合自学者）

## 升级（已有 Phase）

### Phase 2: 图像扩散
- HF Diffusion Course：从"主教材"降为"动手补充"
- 新增 Stanford CME296 Spring 2026（进阶补充）

### Phase 3: 视频模型
- HunyuanVideo 1.5：时间线纠错（inference 2025-11-20、training 2025-12-05，**不是** 2026-05-04）
- 标题加 `★★★ · 消费级首选`
- 新增 4 张工具卡：ComfyUI 视频工作流、Ostris ai-toolkit、ROCm Wan 2.2 教程、DiffSynth-Studio
- 工具策略：从"DiffSynth 唯一"改为 finetrainers / ai-toolkit / DiffSynth **三选一并列**

### Phase 4: 数据 + 评测
- VBench → **VBench-2.0**（5 维 18 子维评估 intrinsic faithfulness）作为主基准
- 新增 Video-Bench（人类偏好对齐，CVPR 2025）
- 新增 VBench Leaderboard + I2V Arena
- 新增 GenVidBench（AI 视频检测，AAAI 2026）
- 新增 Survey of Video Diffusion Models (TMLR'25, v3 2026-02)

### Phase 5: 规模化 + 商用
- NVIDIA Cosmos：升级到 **2.5**（Predict 2.5 + Transfer 2.5 + Reason 2，2026 CES 发布）
- 论文链接更新到 arXiv 2511.00062

### License 对比表
- 新增"闭源 API"分组：Sora 2 / Kling 3.0 / Veo 3.1 / Wan 2.5+ / Runway Gen-4-4.5
- LTX-2 行扩展为 LTX-2 / LTX-2.3

### 硬件指南
- 新增 Phase 0 行（无 GPU）
- 新增 Phase 1.5 行（CPU/4090）
- 新增 Phase 3.5 行（6GB+ 显存即可跑 Helios 蒸馏版）

### 必读论文清单
从 12 篇扩展到 20 篇，新增：
- 13: Intro to Flow Matching and Diffusion Models (2025)
- 14: Survey of Video Diffusion Models (TMLR'25 v3, 2026-02)
- 15: CausVid (CVPR 2025)
- 16: Causal Forcing (ICML 2026)
- 17: VBench-2.0 (2025)
- 18: Video-Bench (CVPR 2025)
- 19: HunyuanVideo 1.5 Tech Report (2025-11)
- 20: Cosmos: World Simulation for Physical AI (2025-11)

## UX 改进

### 资源动作标签（read / run / train / evaluate）
所有 70 张资源卡片都打了至少一个动作标签：

- `read` — 论文 / 综述 / 文档（理论性）
- `run` — 平台 / 工具 / 课程 lab（运行 inference 或跑 demo）
- `train` — 训练框架 / 微调工具 / 数据集（用来训模型）
- `evaluate` — 评测工具 / 排行榜（用来量化模型质量）

让你一眼看出"这个链接拿来干嘛"，避免学习路径变成"光收藏不行动"的论文清单。

### Hero 区
- 加 V2 角标
- tag-row 突出 Flow Matching、AR-Diffusion、闭源/开源全景
- 加"↩︎ 仍想看 V1"链接

### 导航栏
- 新增 P0 / P1.5 / P3.5 入口
- 原"全景"改成"P0 · 2026 全景" + 新增"架构组件"指向 `#overview`

### Footer
- 加 V2 标识 + V1 链接
- 加 V2 vs V1 摘要 + 下次复审日期

## 时间线纠错（来自 Codex 审查）

| 项目 | V1 / 调研稿原版 | V2 修正后 |
|---|---|---|
| Sora 2 | "2026-04 取代 Sora 1" | 2025-09-30 与 iOS Sora app 同发；2026-04-26 是 app 下线、2026-09-24 API 停用 |
| HunyuanVideo 1.5 | "2026-05-04 才完整开源" | inference 2025-11-20、training 2025-12-05 |
| LTX-2.3 | "2026-03-05" | 2026-03-08（官博） |
| DiffSynth-Studio | "降为备选" | 与 finetrainers / ai-toolkit 并列三选一 |
| Mamba 视频生成 | "无重大成果" | 仍是边缘方向，VideoSSM 等工作存在 |

## 还没做（V3 候选）

- UI 视觉升级（V2 沿用 V1 视觉，UI 留待 V3）
- video-model-changelog 自动化（每月 GitHub Action 抓取）
- 中文社区课程的系统调研（覆盖弱，本次未深入）
- Karpathy 是否有视频/扩散方向新作（持续关注）

## 调研依据

V2 内容选择基于 2026-05-07 的 8 阶段系统调研 + Codex 独立审查，调研全文存档于：
`~/Obsidian/ToKnow/Claude/视频大模型学习路径-2026-05-Research.md`

下次复审建议 2026-07-01 前。
