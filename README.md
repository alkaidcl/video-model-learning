# 🎬 视频大模型训练学习路线

> 从零基础到商用级视频生成模型（SeedDance 2.0 级别）的系统化学习门户

## 🌐 在线访问

**GitHub Pages**: 部署后访问 `https://你的用户名.github.io/video-model-learning/`

## 📋 内容概览

| 阶段 | 内容 | 预计周期 |
|------|------|----------|
| **Phase 0** | 数学 + Python + 深度学习基础 | 4-6 周 |
| **Phase 1** | Transformer + 视觉基础 (ViT, CLIP, VAE) | 4-6 周 |
| **Phase 2** | 扩散模型 + 图像生成 (DDPM → LDM → DiT) | 6-8 周 |
| **Phase 3** | 视频生成模型专项 (Wan2.1, CogVideoX, Sora) | 6-8 周 |
| **Phase 4** | 实战训练路线 (LoRA → 微调 → 从头训练) | 8-16 周 |
| **Phase 5** | 商用化 (推理加速, 数据飞轮, 安全合规) | 持续 |

## 🔗 核心资源速查

### 开源视频模型
- [Wan2.1](https://github.com/Wan-Video/Wan2.1) — 阿里万相，当前最强开源视频模型
- [CogVideoX](https://github.com/THUDM/CogVideo) — 清华智谱，代码清晰适合学习
- [HunyuanVideo](https://github.com/Tencent/HunyuanVideo) — 腾讯混元，13B 工业级参考
- [Open-Sora](https://github.com/hpcaitech/Open-Sora) — 完整训练框架

### 必学课程
- [Hugging Face Diffusion Course](https://huggingface.co/learn/diffusion-course) — 扩散模型最佳入门
- [3Blue1Brown 神经网络](https://www.3blue1brown.com/topics/neural-networks) — 直觉建立
- [Stanford CS231n](https://cs231n.stanford.edu/) — 计算机视觉基础
- [fast.ai](https://course.fast.ai/) — 实践导向深度学习

### 必读论文 Top 5
1. [DDPM](https://arxiv.org/abs/2006.11239) — 扩散模型奠基
2. [Latent Diffusion](https://arxiv.org/abs/2112.10752) — 潜空间扩散
3. [DiT](https://arxiv.org/abs/2212.09748) — Diffusion Transformer
4. [Flow Matching](https://arxiv.org/abs/2210.02747) — 新一代训练范式
5. [Sora 技术报告](https://openai.com/index/video-generation-models-as-world-simulators/) — 视频世界模拟器

## 🚀 快速部署

```bash
git clone https://github.com/你的用户名/video-model-learning.git
cd video-model-learning
# 开启 GitHub Pages: Settings → Pages → Source: main branch
```

或者本地预览：
```bash
python3 -m http.server 8080
# 访问 http://localhost:8080
```

## 📝 License

MIT — 自由使用和修改
