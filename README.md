# 卷卷冷知识短片 V2

一个为固定 3D 卡通角色“卷卷”设计的 Codex Skill，用于制作经过事实核查的竖屏冷知识短片，并将职场知识承接为“慢拾光”应用中的 7 分钟训练卡。

## 能做什么

- 生成 8–25 秒卷卷 3D 冷知识短片选题和剧本
- 写剧本时先展示“序幕—第一幕—第二幕—第三幕—尾镜”的可读故事大纲，再展开分镜和制作细节
- 每次生成或改写剧本都自动保存独立 Markdown 文件，递增版本、保留旧稿，并在回复中提供文件链接
- 输出稳定的首帧、尾帧和图生视频提示词
- 支持 LIBTV 分镜协作
- 保持卷卷角色外形、配色、验证环和性格一致
- 制作面向成年人的职场认知、表达、信息判断与安全知识
- 为每条职场视频生成对应的慢拾光训练卡、理解题、片尾 CTA 和渠道追踪字段
- 输出普通冷知识或职场冷知识的封面及发布文案

## 目录结构

```text
juanjuan-cold-fact-shorts-v2/
├── SKILL.md
├── agents/openai.yaml
├── assets/juanjuan-fresh-mint-reference.png
└── references/
    ├── story-outline.md
    ├── prompt-format.md
    ├── publishing-style.md
    └── workplace-slowlight.md
```

## 安装

将本仓库克隆到 Codex 的全局 Skills 目录：

```powershell
git clone https://github.com/tomfun3222-lonlydance/juanjuan-cold-fact-shorts-v2.git "$env:USERPROFILE\.codex\skills\juanjuan-cold-fact-shorts-v2"
```

重新打开 Codex 后即可使用。

## 使用示例

普通冷知识：

```text
$juanjuan-cold-fact-shorts-v2 帮我给卷卷策划 5 个可以在 20 秒内讲清楚的动物冷知识选题。
```

职场与慢拾光联动：

```text
$juanjuan-cold-fact-shorts-v2 制作一期关于任务切换的职场冷知识短片，并生成对应的慢拾光训练卡。
```

完整制作交付：

```text
$juanjuan-cold-fact-shorts-v2 把这个选题做成完整剧集，输出事实来源、剧本、首尾帧、图生视频提示词、封面和发布文案。
```

只展开故事大纲：

```text
$juanjuan-cold-fact-shorts-v2 把“方形泡泡棒为什么吹出圆泡泡”拓展成 24 秒剧本，按序幕、第一幕、第二幕、第三幕、尾镜展示，先不展开生成提示词。
```

剧本首先在回复正文中展示标题、类型、时长建议、基调、场景动作与逐字对白；每次生成或改写时同时保存独立版本文件，包括只写大纲。默认归档到当前工作区的 `episodes/{日期}_{主题}/`，改稿递增版本并保留旧稿，回复附文件链接。完整制作包与大纲使用相同版本号并互相链接。格式及保存规范见 [references/story-outline.md](references/story-outline.md)。

## 两个角色的分工

- **卷卷**：发现异常、提出问题、验证事实，负责短视频传播。
- **小糯**：在慢拾光中陪伴训练、记录心得与成长。

联动表达：**卷卷发现，小糯陪你练会。**

## 内容原则

- 核心事实必须有直接、可点击的权威来源。
- 不把相关性说成因果，不编造心理学效应。
- 劳动法、医疗心理、网络安全和财务内容使用当前官方来源并说明适用范围。
- 生成模型不直接绘制字幕、Logo、二维码或水印，文字统一后期添加。
- 不虚构合作案例、用户评价、成交量或效果承诺。

## 版本说明

V2 保留原版的自然与科学冷知识能力，新增职场成年人语气、慢拾光训练卡映射、渠道追踪和快速验证模式。原版 Skill 可继续独立使用。
