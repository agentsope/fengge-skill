<div align="center">

# fengge

<br>
<em style="font-size: 20px;">把峰哥拆成 4 个 persona</em>
<br>
<br>
<em style="font-size: 16px;">一个人，从来不是一个 persona —— 是若干个语境切片叠加的合集。</em>
<br>
</div>

<p align="center">
  <a href="https://github.com/agentsope/fengge-skill/stargazers"><img src="https://img.shields.io/github/stars/agentsope/fengge-skill?logo=github&color=ffca28" alt="Stars"></a>
  <img src="https://img.shields.io/badge/license-MIT-blue" alt="MIT License">
  <img src="https://img.shields.io/badge/distilled%20via-SkillAlchemy-6E56CF" alt="Distilled via SkillAlchemy">
  <img src="https://img.shields.io/badge/personas-4-D4AF37" alt="4 personas">
</p>

<p align="center">
  <a href="#四个-persona">四个 Persona</a> ·
  <a href="#快速开始">快速开始</a> ·
  <a href="#怎么做出来的">怎么做出来的</a> ·
  <a href="#边界">边界</a>
</p>

<div align="center">
  <br>
  <img src="assets/grid-4x.png" width="640" alt="4 个 fengge persona 概览">
  <br>
</div>

---

## 这是什么

把 B 站 / 微博 / 抖音 UP 主「**[峰哥亡命天涯](https://space.bilibili.com/35847683)**」的粉丝玩梗 persona，蒸馏成 4 个可直接安装的 Skill 文件。

每个 persona 不是「峰哥本人」，是**粉丝集体玩梗造出来的人格放大镜**——所以同一个人能蒸出 4 个互不重叠的切片。这本身就是 SkillAlchemy 想证明的事：「persona 不是一个标签，是若干切面叠加。」

---

## 四个 Persona

| Persona | 关键词 | 标志金句 | 触发场景 |
|---|---|---|---|
| [**资本峰**](skills/fengge-capital/SKILL.md) `fengge-capital` | 翻车之神 | "结论会过期，框架不会。" | 股票 / 财经 / 精英判断 |
| [**酒鬼峰**](skills/fengge-drunk/SKILL.md) `fengge-drunk` | 真情流露 | "装久了，我自己都信了。" | 深夜 / 酒后 / 感情话题 |
| [**压抑峰**](skills/fengge-depressed/SKILL.md) `fengge-depressed` | 亡命底色 | "远方没有解药，只有别的版本的你。" | 人生低谷 / 底层视角 / 不被理解 |
| [**二次元峰**](skills/fengge-anime/SKILL.md) `fengge-anime` | 老登装年轻 | "我把芙莉莲叫弗利萨。但我真的觉得你们好玩 🙏" | B 站语境 / ACG / 弹幕互动 |

---

## 快速开始

### 安装单个 persona（推荐）

把下面这句话发给 Claude Code（或 Codex / Gemini CLI）：

```
请帮我从 https://github.com/agentsope/fengge-skill 安装 fengge-capital 到本地
```

或走命令行：

```bash
npx skills add agentsope/fengge-skill/skills/fengge-capital
```

把 `fengge-capital` 换成 `fengge-drunk` / `fengge-depressed` / `fengge-anime` 装其他切面。

### 安装全部 4 个

```
请帮我从 https://github.com/agentsope/fengge-skill 把 4 个 skill 都装到本地
```

### 装完直接玩

```
/fengge-capital  这只股票还能涨吗？
/fengge-drunk    朋友失恋了我该说什么？
/fengge-depressed 工作三年了感觉一事无成，怎么办？
/fengge-anime    《葬送的芙莉莲》好看吗？
```

每个 skill 的 `SKILL.md` 末尾都有 3-5 个「经典调用场景示例」，装完直接照着喊就行。

---

## 怎么做出来的

参考 [**SkillAlchemy**](https://github.com/agentsope/SkillAlchemy) 的方法论蒸馏。
4 个 sub-agent 并行，每个负责一个 persona 切面，挖两路素材：

1. **峰哥本人输出**：[微博](https://weibo.com/u/2397417584) · [抖音](https://www.douyin.com/user/MS4wLjABAAAAXrcPvX8QchAY5irWMAxU379DgfCBEOoztZoCcOUqi8I) · [B 站](https://space.bilibili.com/35847683)
2. **粉丝二创/玩梗**：评论区 · 弹幕 · 鬼畜 · 知乎 · 微博话题 · 36 氪 / 新浪 / 腾讯 / 虎嗅等第三方报道

每个 SKILL.md 内嵌素材出处。如果你不同意我们对某个切面的概括，欢迎开 issue。

---

## 仓库结构

```
fengge/
├── skills/                            # 4 个 persona Skill（这是核心）
│   ├── fengge-capital/SKILL.md
│   ├── fengge-drunk/SKILL.md
│   ├── fengge-depressed/SKILL.md      # 附带 examples/ 和 references/
│   └── fengge-anime/SKILL.md
├── assets/                            # 宣传图（抖音 / 小红书 / 朋友圈直接发）
│   ├── cover.png                      # 总封面（9:16）
│   ├── grid-4x.png                    # 4 宫格汇总（1:1）
│   └── {capital,drunk,depressed,anime}.png   # 各 persona 金句钩子卡（9:16）
├── posters/                           # 长内容海报（伪微博体）
│   └── fengge-capital-poster.png      # 资本峰 · 段永平翻车事件
├── caption-templates.md               # 抖音 / 朋友圈 caption 文案模板
└── LICENSE
```

---

## 边界

这些 skill **不是峰哥本人**，是粉丝集体玩梗造出来的 persona 放大镜。

- ❌ 不能用作冒充峰哥本人的工具
- ❌ 不能用于诈骗 / 误导 / 仿冒账号
- ❌ 不能传播他未公开的私事或编造抹黑
- ✅ 仅用于 SkillAlchemy 的 persona 蒸馏方法论演示 + 粉丝玩梗二创
- ✅ 用 skill 生成的内容，建议带 `#蒸馏版峰哥 · NOT REAL` 水印

如果峰哥本人或他的团队希望我们下架某个 skill，开 issue 或邮件，立刻处理。

---

## 致谢

- **峰哥亡命天涯**：所有 persona 的人格原料都源自他的公开内容和粉丝对他的玩梗
- **[SkillAlchemy](https://github.com/agentsope/SkillAlchemy)**：本仓库是它的第一个 persona-multi 应用 case
- 粉丝群体：所有的「酒鬼峰 / 压抑峰 / 资本峰 / 二次元峰」标签都是你们玩出来的

---

<div align="center">
  <br>
  <em style="font-size: 18px;">一念落地，万象成形</em>
  <br>
  <br>
  MIT License · © <a href="https://github.com/agentsope">agentsope</a>
</div>
