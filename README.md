# 数字化转型的投资结构优化效应：第五届香樟数字经济论坛 Beamer

这是为“第五届香樟数字经济论坛”准备的 20 分钟学术汇报 Beamer 项目，基于 `beamer-universal-academic-template` 创建。

内容依据：

- Gmail 邮件《第五届香樟数字经济论坛入选通知》
- 最新论文文档：`/Users/eamonsuen/Documents/GitHub/Paper-Digital-Real-Integration/04_Writing/数字化转型的投资结构优化效应_260424_YimingV3.docx`

## 特点

- 基于 `XeLaTeX + ctex + biblatex`
- 支持中英文混排
- 按章节拆分内容，便于长期维护
- 预留 `figures/`、`tables/`、`bib/` 和 `fonts/` 目录
- 使用 `output/` 统一存放编译产物

## 目录

```text
beamer-universal-academic-template/
├── README.md
├── .gitignore
├── main.tex
├── references.bib
├── sections/
├── figures/
├── tables/
├── bib/
├── fonts/
└── output/
```

## 编译

推荐使用：

```bash
latexmk -xelatex -outdir=output main.tex
```

清理辅助文件：

```bash
latexmk -c -outdir=output main.tex
```

## 会议信息

- 会议时间：2026-05-10
- 会议地点：中国长春
- 报到时间：2026-05-09 14:00
- 汇报时长：20 分钟
- 回执截止：2026-05-04

详细备忘见 [notes/conference_brief.md](/Users/eamonsuen/Documents/GitHub/beamer-xiangzhang-digital-economy-forum-2026/notes/conference_brief.md)。

## 使用说明

1. 修改 `main.tex` 中的标题、作者、机构和日期。
2. 按需编辑 `sections/` 下各章节文件。
3. 将图片和 logo 放入 `figures/`。
4. 将表格片段放入 `tables/`。
5. 将文献维护在 `references.bib` 或 `bib/references.bib`。

## 字体说明

模板默认直接使用本机固定路径下的字体仓库：

- `/Users/eamonsuen/Documents/GitHub/latex-chinese-fonts`

当前默认配置：

- 英文正文字体：`TimesNewRoman.ttf`
- 英文无衬线：`Helvetica.ttf`
- 英文等宽：`Courier.ttf`
- 中文正文字体：`FangSong.ttf`
- 中文无衬线：`STHeiti.ttf`
- 中文等宽替代：`SimHei.ttf`

这样做比依赖系统字体名更稳定，原因是：

- 不依赖 Fontconfig 或系统字体注册状态
- 字体粗体、斜体映射可以显式控制
- 换机器后只要该仓库路径不变，编译结果更一致

如果你希望针对单个项目使用自带字体，也可以把字体文件放入：

- `fonts/serif/`
- `fonts/sans/`
- `fonts/mono/`

然后在 [main.tex](/Users/eamonsuen/Documents/GitHub/beamer-universal-academic-template/main.tex) 中取消对应注释并调整文件名。

## 建议

- 若是正式汇报，建议把 `logo/logo.pdf` 替换为你的学校或机构标识。
- 若文献库只保留一个版本，建议统一使用根目录的 `references.bib`。
