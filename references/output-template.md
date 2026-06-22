# Default Output Template

Use this format unless the user requests a shorter, English-only, JSON, table, or other custom format. Keep each image section independent and numbered in the original upload order.

```markdown
第 1 张图片 -> image-2 反推 Prompt 1

客观画面分析：
- 主体：
- 主体状态：
- 构图：
- 镜头：
- 光影：
- 色彩：
- 场景：
- 材质：
- 风格：
- 画质：

微观细节反推：
- 动作松弛感：
- 头部角度：
- 脸部朝向：
- 表情调动：
- 眼神方向：
- 瞳孔颜色：
- 瞳孔聚焦 / 涣散程度：
- 嘴唇状态：
- 眉眼状态：
- 皮肤质感：
- 手部状态：
- 身体重心：
- 服装褶皱：
- 发丝状态：

摄影与构图反推：
- 画幅比例：
- 主体位置：
- 主体占比：
- 画面裁切：
- 前景 / 中景 / 背景：
- 视觉重心：
- 构图类型：
- 相机角度：
- 机位高度：
- 拍摄距离：
- 焦距定稿：
- 光圈定稿：
- 快门定稿：
- ISO 定稿：
- 曝光状态：
- 白平衡定稿：
- 滤镜 / 后期定稿：

image-2 生成逻辑反推：
...

最终 image-2 Prompt：
...

Avoid / Do not include：
...

置信度标注：
- 高置信：
- 中置信：
- 低置信：

自检：
- 图片编号是否正确：是 / 否
- 是否遗漏图片：是 / 否
- 是否一图一 Prompt：是 / 否
- 构图判断是否具体：是 / 否
- 相机参数是否作为确定性生成参数输出：是 / 否
- 最终 Prompt 是否没有“约 / 可能 / 看起来像 / 视觉估算”等模糊词：是 / 否
- 最终 Prompt 是否符合 image-2 自然语言规则：是 / 否
- 是否避免关键词堆砌：是 / 否
- 是否避免编造不可见细节：是 / 否
- 是否可以直接复制给 image-2 使用：是 / 否
```

For multiple images, repeat the same structure with continuous numbering:

- `第 2 张图片 -> image-2 反推 Prompt 2`
- `第 3 张图片 -> image-2 反推 Prompt 3`
- Continue until the number of sections exactly equals the number of images.

For many images, output in batches only if necessary. Keep numbering continuous and state the batch range, for example `本次输出第 1-5 张，下一批从第 6 张继续。`
