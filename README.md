# talent-brief

一个 Codex skill：把飞书/会议纪要、简历片段、聊天记录和用户补充评价，压缩为可直接转发给 founder、HRD 或招聘群的中文候选人推荐语。

它默认产出一段精炼、具体、隐私安全的 brief，而不是面评、打分报告或完整履历复述。

## 安装

在 Codex 中输入：

```text
用 $skill-installer 从 GitHub 安装 FZVincent2006/talent-brief 仓库中的 skills/talent-brief。
```

也可以在终端运行：

```bash
python ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo FZVincent2006/talent-brief \
  --path skills/talent-brief
```

安装完成后，在下一轮对话中使用：

```text
用 $talent-brief 综合这段飞书交流记录和候选人简历，写一版可发给 founder/HRD 群的推荐语。
```

## 输入

- 飞书/Lark 面试或交流纪要
- PDF、文本或聊天中的候选人简历
- 聊天记录、候选人信息和历史推荐语
- 对候选人的主观评价、目标公司或目标 JD

当同时提供简历和交流记录时，skill 会以简历校准履历、项目与数据，以交流记录补充最新状态、机会偏好和 base。

## 隐私

skill 默认不会保留原始材料，也会省略联系方式、薪酬与其他不应群发的信息；敏感的现公司默认改写为行业/公司类型，除非明确说明可公开。

## 许可证

[MIT](LICENSE)
