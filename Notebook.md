# Table

Tip: edit your data in excel (2016 is ok), then use [`Excel2LaTeX`](https://ctan.org/pkg/excel2latex) to get LaTeX code.

+ 如果有行、列合并，需要`\usepackage{multirow}`，`\usepackage{multicol}`。
+ 调整`array`或`tabular`环境内的列间距：`\renewcommand\arraystretch{1.1}`。默认值是1，即不调整。经验上，列间距较大比较好看。
+ 在项目名称和数据列之间，可以采用双竖线，即`||`。视觉效果好。
+ 设置表格位置：`\begin{table}[htbp]`分别表示此处、顶部（所处页）、底部、单独一页。如果都加，表示让系统自己决定。如果加感叹号，表示强制。

```
\usepackage{multirow}

\begin{table}[!t]
	\vspace{-0.0em}
	\renewcommand\arraystretch{1.1}
	\centering
	\footnotesize
	\caption{Performance of our PQF detector on test sequences.}
	\begin{tabular}{|l|c||c c c|}
		\hline
		\multirow{2}{*}{Approach} & \multirow{2}{*}{QP} & Precision & Recall & $F_1$-score \\ [-0.3em]
		
		& & ($\%$) & ($\%$) & ($\%$) \\
		
		\hline
		\multirow{5}{*}{MFQE 2.0} & 22 & 98.01 & 98.09 & 98.05 \\
		
		% \cline{2-5}
		& 27 & 97.65 & 98.27 & 97.96 \\
		
		%\cline{2-5}
		& 32 &97.92 & 97.88 & 97.90 \\
		
		\cline{2-5}
		& 37 & \textbf{97.25} & \textbf{97.47} & \textbf{97.36} \\
		
		%\cline{2-5}
		& 42 & \textbf{98.14} & \textbf{97.10} & \textbf{97.62} \\
		
		\hline
		\multirow{2}{*}{MFQE 1.0} & 37 & 90.68 & 92.11 & 91.09 \\
		
		%\cline{2-5}
		& 42 & 93.98 & 90.86 & 92.23\\
		
		\hline
		
	\end{tabular}
	\label{sc}
	\vspace{-0.0em}
\end{table}
```

+ latex字体大小，有小到大依次为：\tiny \scriptsize \footnotesize \small \normalsize \large \Large \LARGE \huge \Huge
+ 字符间隔调整，前两个的间隔较大，后面三个较小，最后一个是负间隔： \quad \qquad \, \: \; \!

三线表：

+ 引入宏包：`\usepackage{booktabs}`
+ 顶部线：`\toprule`，又黑又粗
+ 中部线：`\midrule`，又白又细
+ 底部线：`\bottomrule`：和顶部差不多



