# 视频大模型训练学习路线 V2 · 2026-Q2

> V1 (2026-03-13 创建) 的 2026-Q2 升级版。V1 仍可访问、未做改动。

## 在线访问

- **V2（当前版）**：https://alkaidcl.github.io/video-model-learning/v2/
- **V1（历史版）**：https://alkaidcl.github.io/video-model-learning/

## V2 是什么

距 V1 创建已 2 个月。视频生成生态在这 2 个月发生了几件大事，V2 是这些变化的回应：

- Flow Matching 已成为视频模型主流训练目标（DDPM 1000 步 → FM 10 步同质量）
- 自回归扩散在 2026-Q1-Q2 集中爆发（CausVid → Causal Forcing → Helios），实时长视频成为可能
- 闭源商业模型（Sora 2 / Kling 3.0 / Veo 3.1 / Wan 2.5+ / Runway Gen-4.5）独立成线
- 评估标准升级到 VBench-2.0 + Video-Bench
- HunyuanVideo 1.5 在 2025-11/12 完整开源（消费级首选）
- NVIDIA Cosmos 2.5 (CES 2026) 把 physical AI / world model 拉成独立分支

## 6 阶段课程结构

| 阶段 | 内容 | 周期 | 是否 V2 新增 |
|------|------|------|-------------|
| **Phase 0** | 2026 视频生成全景：闭源基线 + 开源主力 | 入门即看 | ✅ 新增 |
| **Phase 1** | PyTorch + 训练循环（Karpathy） | 2-3 周 | 保留 |
| **Phase 1.5** | Flow Matching 一周冲刺（MIT 6.S184） | 1 周 | ✅ 新增 |
| **Phase 2** | 图像扩散 DDPM → LDM → DiT + LoRA | 3-4 周 | 升级（HF 课程降为辅助 + Stanford CME296） |
| **Phase 3** | 视频模型推理 + LoRA + ComfyUI 工作流 | 4-6 周 | 升级（加 ComfyUI/ai-toolkit/ROCm/DiffSynth 四件套） |
| **Phase 3.5** | 自回归扩散趋势章（CausVid→Causal Forcing→Helios） | 2-3 周 | ✅ 新增 |
| **Phase 4** | 数据 + VBench-2.0 + Video-Bench + 综述 | 4-6 周 | 升级（VBench-2.0 主推 + Video-Bench + GenVidBench） |
| **Phase 5** | Scale-up + 商用 + Cosmos 2.5 | 长期 | 升级（NVIDIA Cosmos 2.5 + xDiT） |

每条资源都打了 `read` / `run` / `train` / `evaluate` 四类动作标签——一眼就能看出这个链接是用来"读"还是"跑"还是"训"。

## 与 V1 的关系

- V1 一字未改、仍在原 URL 工作
- V2 不是替换 V1，而是平行迭代的新版本
- 如果你已收藏 V1，链接仍有效；想看 2026-Q2 升级内容请用 V2 URL

完整变更说明见 [v2/changelog.md](changelog.md)。

## 调研依据

V2 的资源选择基于 2026-05-07 的系统调研，全文存档于本地 Obsidian：
`~/Obsidian/ToKnow/Claude/视频大模型学习路径-2026-05-Research.md`

调研经过 8 阶段流程（日期锚定 → 多源搜索 → 时效筛选 → 综合分析 → 自我批判 → Codex 独立审查 → 修订）。Codex 审查后纠正了若干时间线硬伤（Sora 2 / HunyuanVideo 1.5 / LTX-2.3）和漏掉的方向（Kling 3.0 / NVIDIA Cosmos 2.5 / ComfyUI workflow）。

## 下次复审

建议 2026-07-01 前重做一轮。AI 视频生态以月为单位变化。

## License

MIT — 自由使用和修改
