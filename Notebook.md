# Table

Tip: edit your data in excel (2016 is ok), then use [`Excel2LaTeX`](https://ctan.org/pkg/excel2latex) to get LaTeX code.

+ 如果有行、列合并，需要`\usepackage{multirow}`。
+ 调整`array`或`tabular`环境内的列间距：`\renewcommand\arraystretch{1.1}`。默认值是1，即不调整。经验上，列间距较大比较好看。

```
\usepackage{multirow}

\begin{table}[htbp]
  \renewcommand\arraystretch{1.1}
  \centering
  \caption{Performance of original and modified DS-CNN}
  \begin{tabular}{|c|c|c|crc|}
    \hline
    QP    & \multicolumn{2}{c|}{DS-CNN} & original & modified & $\Delta$ (\%) \\
    \hline
    \multirow{19}[12]{*}{37} & \multirow{2}[2]{*}{A} & \multicolumn{1}{l|}{\textit{Traffic}} & 0.286  & \textbf{0.299 } & 4.5 \\
    &       & \multicolumn{1}{l|}{\textit{PeopleOnStreet}} & 0.445  & \textbf{0.465 } & 4.5  \\
    \cline{2-6}              & \multirow{5}[2]{*}{B} & \multicolumn{1}{l|}{\textit{Kimono}} & 0.216  & \textbf{0.280 } & 29.6  \\
    &       & \multicolumn{1}{l|}{\textit{ParkScene}} & 0.180  & \textbf{0.188 } & 4.4  \\
    &       & \multicolumn{1}{l|}{\textit{Cactus}} & 0.197  & \textbf{0.259 } & 31.5  \\
    &       & \multicolumn{1}{l|}{\textit{BQTerrace}} & 0.277  & \textbf{0.298 } & 7.6  \\
    &       & \multicolumn{1}{l|}{\textit{BasketballDrive}} & 0.309  & \textbf{0.317 } & 2.6  \\
    \cline{2-6}              & \multirow{4}[2]{*}{C} & \multicolumn{1}{l|}{\textit{RaceHorses}} & 0.284  & \textbf{0.305 } & 7.4 \\
    &       & \multicolumn{1}{l|}{\textit{BQMall}} & 0.312  & \textbf{0.361 } & 15.7  \\
    &       & \multicolumn{1}{l|}{\textit{PartyScene}} & 0.190  & \textbf{0.191 } & 0.5  \\
    &       & \multicolumn{1}{l|}{\textit{BasketballDrill}} & 0.366  & \textbf{0.387 } & 5.7  \\
    \cline{2-6}              & \multirow{4}[2]{*}{D} & \multicolumn{1}{l|}{\textit{RaceHorses}} & 0.343  & \textbf{0.358 } & 4.4\\
    &       & \multicolumn{1}{l|}{\textit{BQSquare}} & 0.189  & \textbf{0.190 } & 0.5  \\
    &       & \multicolumn{1}{l|}{\textit{BlowingBubbles}} & 0.208  & \textbf{0.243 } & 16.8  \\
    &       & \multicolumn{1}{l|}{\textit{BasketballPass}} & 0.350  & \textbf{0.375 } & 7.1  \\
    \cline{2-6}              & \multirow{3}[2]{*}{E} & \multicolumn{1}{l|}{\textit{FourPeople}} & 0.412  & \textbf{0.481 } & 16.7 \\
    &       & \multicolumn{1}{l|}{\textit{Johnny}} & 0.348  & \textbf{0.389 } & 11.8  \\
    &       & \multicolumn{1}{l|}{\textit{KristenAndSara}} & 0.475  & \textbf{0.500 } & 5.3  \\
    \cline{2-6}              & \multicolumn{2}{c|}{Average} & 0.299  & \textbf{0.327 } & 9.4  \\
    \hline
    42    & \multicolumn{2}{c|}{Average} & 0.301  & \textbf{0.330 } & 9.6 \\
    \hline
    32    & \multicolumn{2}{c|}{Average} & 0.288  & \textbf{0.291 } & 1.0 \\
    \hline
    27    & \multicolumn{2}{c|}{Average} & 0.261  & \textbf{0.284 } & 8.8 \\
    \hline
    22    & \multicolumn{2}{c|}{Average} & 0.263  & \textbf{0.276 } & 4.9 \\
    \hline
  \end{tabular}%
  \label{tab:addlabel}%
\end{table}%
```
