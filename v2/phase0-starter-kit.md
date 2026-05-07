# Phase 0 启动包 · 6 个闭源模型实测

> 目标：用 1-2 个晚上把 6 个商业闭源模型都跑一遍，建立你自己的"能力对照基线"。这是 Phase 1 之前最重要的一件事——不知道闭源 SOTA 长什么样，你就没法判断开源模型是"好用了"还是"差远了"。

价格/访问门槛核对日期：**2026-05-07**。AI 视频价格变动以月计，下次启动前请重新核对。

---

## 总览：6 个模型 × 访问方式 × 国内可达性

| 模型 | 入口（国内不翻墙） | 入口（境外/VPN） | 起步成本 | 推荐起点 | 国内直达？ |
|------|------------------|---------------|---------|---------|----------|
| **即梦 / Seedance 2.0** (字节) | [jimeng.jianying.com](https://jimeng.jianying.com/) | 同 | ¥1 试用会员解锁 2.0 + 新用户 2 次免费 + 260 积分 | 即梦 Web | ✅ |
| **豆包 Video** (字节) | 豆包 App（移动端） | — | 每日 10 次免费（需飞书 beta 群） | 移动 App | ✅（需 +86 手机号） |
| **Wan 2.5/2.6/2.7** (阿里) | [Aliyun Model Studio](https://help.aliyun.com/zh/model-studio/) | 同 | 阿里云免费额度 + 按调用计费 | API 调用 | ✅ |
| **Kling 3.0** (快手) | — | [kling.ai](https://kling.ai/app/membership/membership-plan) | **Ultra $180/月**（独占 3.0 早期访问） | Web | 需 VPN + 国际卡 |
| **Veo 3.1** (Google) | — | [Google AI Pro](https://gemini.google.com/) ($19.99/月) 或 [Vertex AI](https://cloud.google.com/vertex-ai/generative-ai/pricing) ($0.05/秒 Lite) | $19.99/月起 | Gemini app 入口 | 需 VPN（API 失败率 15-40%） |
| **Runway Gen-4 / 4.5** | — | [runwayml.com/pricing](https://runwayml.com/pricing) | **免费 125 credits ≈ 25 秒** | 免费试用 | 需 VPN |
| **Sora 2** (OpenAI) | — | API（2026-09-24 停用） | — | **跳过实测**（已退场） | ❌ |

> 提示：Kling 3.0 体验门槛是 6 个里最高的（$180/月）。如果不打算长期付费，可以先订 1 个月、密集跑测试 prompt 后退订。

---

## 0 元 + 低成本启动路径（推荐顺序）

### 第 1 晚（免费/低成本，2-3 小时跑完）
1. **即梦 Web**（10-15 分钟开通）：[jimeng.jianying.com](https://jimeng.jianying.com/) 注册 → 开通 ¥1 试用会员解锁 Seedance 2.0 → 跑下面 10 条测试 prompt
2. **豆包 App**（如果有 +86 手机号）：装移动端 → 加飞书 beta 群 → 每日 10 次免费
3. **Aliyun Model Studio**：[help.aliyun.com/zh/model-studio](https://help.aliyun.com/zh/model-studio/) → 阿里云账号 → 调 wan2.5-i2v / wan2.7-t2v API（首次有免费额度）
4. **Runway Gen-4**：[runwayml.com](https://runwayml.com/) 注册 → 免费 125 credits → 用 Gen-4 Turbo（5 credits/秒）跑 25 秒

### 第 2 晚（付费试用，可选）
5. **Google AI Pro $19.99/月**：[gemini.google.com](https://gemini.google.com/) 订阅 → Gemini app 里直接生成 Veo 3.1 Fast（90 个/月）
6. **Kling Ultra $180/月**（最贵，跳过也可）：[kling.ai](https://kling.ai/) → 订 1 个月 → 密集跑测试 prompt → 月底前退订

### 不建议投入
- **Sora 2**：已退场（API 2026-09-24 停用，OpenAI 不再投入），看几段官网 demo 视频即可，不必注册付费

---

## 10 条标准测试 prompt 套件（中英双语）

每条 prompt 在 6 个模型上各跑 **1 次**，用同一个 prompt + 默认参数（5 秒 / 默认分辨率 / 默认步数）。**关键**：固定 seed（如果模型支持）+ 不要手动选最佳 take，只看第 1 个输出。

### #1 单人简单动作（基线）
- **中文**：一位年轻女性在咖啡馆窗边看书，阳光从侧面照进来，她缓慢地翻动书页。
- **English**: A young woman reads a book by a café window, sunlight streaming in from the side, slowly turning pages.
- **看什么**：人脸是否变形 / 手指是否扭曲 / 翻页动作是否自然

### #2 复杂镜头运动
- **中文**：从一杯热咖啡的特写镜头，缓慢拉远，露出整个木质书桌和书房，然后再推回特写。
- **English**: Start from a close-up of a steaming coffee cup, slowly zoom out to reveal the entire wooden desk and study room, then push back into close-up.
- **看什么**：镜头运动是否连贯 / 退远后场景是否合理 / 推回后特写是否一致

### #3 物理常识（碎裂）
- **中文**：一只透明玻璃杯从桌边滑落，撞击地面后碎成几块，慢动作拍摄。
- **English**: A transparent glass slips off the edge of a table, hits the floor and breaks into several pieces, in slow motion.
- **看什么**：玻璃碎裂方向是否符合物理 / 重力是否真实 / 碎片是否有合理的弹跳

### #4 多人交互
- **中文**：两个人坐在公园长椅上聊天，左边的人把一杯咖啡递给右边的人。
- **English**: Two people sitting on a park bench chatting; the person on the left hands a coffee cup to the person on the right.
- **看什么**：两个人脸是否独立稳定 / 交接动作是否自然 / 杯子是否变形

### #5 动物动作
- **中文**：一只橘猫从窗台跳到地板上，落地后伸懒腰。
- **English**: An orange cat jumps from a windowsill to the floor, then stretches after landing.
- **看什么**：跳跃轨迹 / 落地缓冲是否合理 / 猫腿数量是否正确（这是 AI 视频经典翻车点）

### #6 文字渲染
- **中文**：一块霓虹灯招牌在雨夜街道闪烁，上面写着"VIDEO 2026"，字体粗体红色。
- **English**: A neon sign flickering on a rainy night street, displaying "VIDEO 2026" in bold red letters.
- **看什么**：文字是否清晰 / 拼写是否正确 / 闪烁节奏是否自然

### #7 风格化
- **中文**：吉卜力风格的雨夜小镇，狭窄石板街道两侧是温暖的灯笼，一位撑红伞的少女缓慢走过。
- **English**: A Ghibli-style rainy night town with narrow stone streets lined with warm lanterns; a girl with a red umbrella walks slowly through.
- **看什么**：风格是否到位（不是真实照片） / 雨滴/灯光/反射是否合理

### #8 长场景一致性
- **中文**：海边日落，海浪从远处推上沙滩，然后退回去，重复 3 次，固定机位。
- **English**: Beach sunset; waves roll in from the distance and pull back, repeated 3 times, fixed camera angle.
- **看什么**：5 秒以上时长一致性 / 海平面是否稳定 / 太阳位置是否变形

### #9 高速运动
- **中文**：一辆 F1 赛车从远处直道高速冲过来，从镜头前呼啸而过，背景产生强烈的运动模糊。
- **English**: A F1 car races down a straight track from far away and roars past the camera with strong motion blur in the background.
- **看什么**：高速运动模糊是否自然 / 车型是否一致 / 路面纹理是否撕裂

### #10 复杂场景（厨房）
- **中文**：一位中国厨师在厨房快速切胡萝卜片，刀光与食材飞溅，背景有蒸汽锅。
- **English**: A Chinese chef quickly slices carrots in a kitchen, knife flashing and ingredients flying, with steaming pots in the background.
- **看什么**：手指是否被切到 / 刀工节奏 / 飞溅的胡萝卜片轨迹

---

## 评分模板（复制到 Excel/Notion 用）

每条 prompt × 每个模型一行。给 5 个维度各打 1-5 分（5 = 完美 / 1 = 严重翻车），最后一栏写 1-2 句主观感受。

| Prompt # | 模型 | 画面清晰度 | 物理一致性 | 主体一致性 | 动作流畅度 | Prompt 遵从度 | 总分 (5 维平均) | 备注 |
|---|---|---|---|---|---|---|---|---|
| #1 | 即梦 |   |   |   |   |   |   |   |
| #1 | 豆包 |   |   |   |   |   |   |   |
| #1 | Wan 2.7 |   |   |   |   |   |   |   |
| #1 | Kling 3.0 |   |   |   |   |   |   |   |
| #1 | Veo 3.1 |   |   |   |   |   |   |   |
| #1 | Runway Gen-4 |   |   |   |   |   |   |   |
| #2 | … | | | | | | | |

跑完 10 × 6 = 60 个视频后，你会有一张**自己的能力地图**——这比任何排行榜都更值得相信，因为这是用你自己关心的场景打的分。

---

## Phase 0 完成标准（出门 checklist）

跑完上面的实测后，确认你能回答：

- [ ] 哪个模型生成的人脸最稳？
- [ ] 哪个模型物理常识最差？（玻璃杯/F1/猫的腿数）
- [ ] 哪个模型对中文 prompt 最敏感？哪个对英文最敏感？
- [ ] 哪个模型 5 秒以上时长一致性最好？
- [ ] 文字渲染谁最准？（#6 招牌）
- [ ] 你做的是创作型项目还是产品型项目？哪个模型最匹配你的需求？
- [ ] 用一句话描述每个模型的"差异化定位"

回答完这些，你就可以开始 Phase 1（PyTorch + Karpathy）——并且**不会再被任何闭源模型的官网 demo 视频"恐吓"**，因为你已经知道它们各自最弱的地方在哪。

---

## 下一步

完成 Phase 0 → 进入 [Phase 1（基础+动手）](./index.html#phase1) → 之后是 [Phase 1.5（Flow Matching）](./index.html#phase15)。

整个 V2 课程结构：[v2/README.md](./README.md) · 完整 V1→V2 差异：[v2/changelog.md](./changelog.md)

**最后核对日期**：2026-05-07。如果你在 2026-07 或更晚才开始 Phase 0，记得先重新核对一下各家价格——AI 视频订阅价格变动以月为单位（Kling Ultra 半年涨了 41%）。
