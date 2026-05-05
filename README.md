# 数字化转型的投资结构优化效应

这是基于 `数字化转型的投资结构优化效应_汇报讲稿.md` 生成的中文学术 Beamer 汇报项目。

## 项目结构

- `main.tex`：Beamer 入口、字体、主题、标题信息、章节顺序与参考文献。
- `sections/01_intro.tex` 至 `sections/05_conclusion.tex`：正式汇报正文。
- `sections/99_appendix.tex`：答辩预案与备用材料。
- `tables/`：正文和附录中调用的回归表片段。
- `references.bib`：正文引用的参考文献。
- `output/main.pdf`：当前编译生成的汇报 PDF。

## 编译

在项目根目录运行：

```bash
latexmk -xelatex -outdir=output main.tex
```

项目使用 `XeLaTeX + ctex + biblatex`。字体路径在 `main.tex` 中的 `\FontRoot` 设置为：

```tex
\newcommand{\FontRoot}{/Users/eamonsuen/Documents/GitHub/latex-chinese-fonts}
```

如果换机器编译，只需要把该路径改为本机 `latex-chinese-fonts` 仓库的位置。

## 内容安排

正文按 20 分钟汇报组织：

1. 研究问题与动机事实
2. 两化融合贯标与融资契约机制
3. ABL/CFL 双重融资摩擦模型
4. 交叠 DID、基准结果、机制检验与效率含义
5. 结论与政策启示

附录保留了讲稿中的常见答辩问题和备用融资表。
