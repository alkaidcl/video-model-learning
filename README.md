# 视频大模型训练学习路线

> 边学边做，从零到商用级视频生成模型

## 在线访问

**GitHub Pages**: https://alkaidcl.github.io/video-model-learning/

## 内容概览

每个阶段都包含理论 + 动手实践，不是学完再练。

| 阶段 | 内容 | 预计周期 |
|------|------|----------|
| **Phase 1** | 基础入门：PyTorch + 训练循环 | 2-3 周 |
| **Phase 2** | 图像扩散：DDPM → LDM → DiT + LoRA 实操 | 3-4 周 |
| **Phase 3** | 视频模型：推理 → 视频 LoRA 微调 | 4-6 周 |
| **Phase 4** | 数据 + 评测：自建数据集 + VBench | 4-6 周 |
| **Phase 5** | 规模化 + 商用：大规模训练 / 推理加速 / 合规 | 长期 |

## 核心资源速查

### 开源视频模型
- [Wan2.1/2.2](https://github.com/Wan-Video/Wan2.1) — 阿里万相，当前最强开源视频模型
- [HunyuanVideo 1.5](https://github.com/Tencent/HunyuanVideo) — 腾讯混元，8.3B 消费级可跑
- [Helios](https://arxiv.org/abs/2603.04379) — 北大，实时长视频生成（2026.3）
- [Open-Sora 2.0](https://github.com/hpcaitech/Open-Sora) — 11B 模型，$200K 训练成本
- [CogVideoX](https://github.com/THUDM/CogVideo) — 清华智谱，代码清晰适合学习

### 必学课程
- [Karpathy Zero to Hero](https://karpathy.ai/zero-to-hero.html) — 神经网络训练循环最佳入门
- [Hugging Face Diffusion Course](https://huggingface.co/learn/diffusion-course) — 扩散模型最佳入门

### 必读论文 Top 5
1. [DDPM](https://arxiv.org/abs/2006.11239) — 扩散模型奠基
2. [Latent Diffusion](https://arxiv.org/abs/2112.10752) — 潜空间扩散
3. [DiT](https://arxiv.org/abs/2212.09748) — Diffusion Transformer
4. [Flow Matching](https://arxiv.org/abs/2210.02747) — 新一代训练范式
5. [Sora 技术报告](https://openai.com/index/video-generation-models-as-world-simulators/) — 视频世界模拟器

## 快速部署

```bash
git clone https://github.com/alkaidcl/video-model-learning.git
cd video-model-learning
# 开启 GitHub Pages: Settings → Pages → Source: main branch
```

或者本地预览：
```bash
python3 -m http.server 8080
# 访问 http://localhost:8080
```

## License

MIT — 自由使用和修改
