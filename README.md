# 产品视觉技能 · Product Visual Skills

两个可单独安装、也可连续使用的 Codex 技能：一张产品图生成六张独立视图，再根据参考海报制作产品宣传图。

## 技能

| 技能 | 输入 | 输出 |
| --- | --- | --- |
| [产品六视图完整安装包](product-six-views.zip) | 一张产品图 | 正、左、右、后、顶、底六张独立图片 |
| [产品参考海报完整安装包](product-reference-posters.zip) | 前面的参考海报＋最后六张独立产品视图 | 每张参考对应一张独立产品海报，并统一名称、型号和文案 |

六视图指六个独立图片文件，每张仅一个视角。

## 安装

分别下载所需的技能压缩包，解压后将 `product-six-views` 或 `product-reference-posters` 文件夹复制到个人 Codex 技能目录。保留各自的 `SKILL.md`、`agents/` 和 `references/`，两个技能可以分别安装。

- [直接下载产品六视图](https://github.com/HH683/product-visual-skills/raw/refs/heads/main/product-six-views.zip)
- [直接下载产品参考海报](https://github.com/HH683/product-visual-skills/raw/refs/heads/main/product-reference-posters.zip)

技能需要宿主提供可用的图像生成或编辑能力，本仓库不包含图像模型或密钥。

## 使用产品六视图

上传一张产品图，输入：

```text
使用 $product-six-views，生成正、左、右、后、顶、底六张独立产品图，并检查3C产品的必要接口和按键。
```

保留原图可确认结构；对不可见的后面、底部、接口等以最少假设补全，并说明哪些是推定。生成图不能代替实物测绘或精确工程图。

## 使用产品参考海报

按顺序上传：先放参考海报，再放产品正、左、右、后、顶、底六张独立图片。输入：

```text
使用 $product-reference-posters，逐张匹配前面参考海报的构图、排版与审美。最后六张是产品的独立六视图，请统一名称、型号和文案，实际生成对应海报。
```

例如：3张参考海报＋6张产品图，生成3张独立海报。各张分别跟随对应参考，不混成通用模板。名称和型号缺省时可以统一创作；未知的性能、价格、认证或功能不会照搬或编造。

## 安装包内文件结构

```text
product-visual-skills/
├── README.md
├── product-six-views/
│   ├── SKILL.md
│   ├── agents/openai.yaml
│   └── references/generation.md
└── product-reference-posters/
    ├── README.md
    ├── SKILL.md
    ├── agents/openai.yaml
    └── references/generation.md
```

完整规则以各技能的 `SKILL.md` 为准。
