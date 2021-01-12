# latex-mould-for-BUAA-bachelor-thesis-2021

北航2021毕业论文latex模板

关于毕业论文格式的具体要求参见“北京航空航天大学本科生毕业设计（论文）手册工科类”，这里只给出.tex内容。

```tex
\documentclass[UTF8, 12pt, a4paper]{ctexart}

\title{\fontsize{36pt}{0}\heiti{毕业设计（论文）}}

\date{}%不显示默认日期
\author{}

%-------------------------目录格式-------------------------%
\usepackage{titletoc}
\titlecontents{section}[2em]{\heiti  \vspace{10pt}}{\contentslabel{1em}}{\hspace*{-4em}}{~\titlerule*[0.6pc]{$.$}~\contentspage}

\titlecontents{subsection}[4em]{\songti}{\contentslabel{2em}}
{\hspace*{-4em}}{~\titlerule*[0.6pc]{$.$}~\contentspage}

%-------------------------英文字体-------------------------%
\usepackage[center]{titlesec}
\usepackage{times}

%-------------------------数字字体-------------------------%
\usepackage[T1]{fontenc}
\usepackage{mathptmx}

%-------------------------插图设置-------------------------%
\usepackage{graphicx}
\usepackage{float}

\usepackage{ragged2e}

%-------------------------页面尺寸-------------------------%
\usepackage{geometry}
\geometry{a4paper,left=3cm,right=2cm,top=3cm,bottom=2.5cm}
\usepackage{setspace}
\renewcommand{\baselinestretch}{1.5}

%---------------------------抬头---------------------------%
\usepackage{fancyhdr}
\fancyhf[F]{}

%---------------------------正文---------------------------%
\begin{document}

%---------------------------------------------------------第一页
%封面部分，包括Logo，毕业设计和题目以及信息
\begin{titlepage}

    %新命令，用于生成指定长度的下划线
    \makeatletter
    \newcommand\dlmu[2][4cm]{\hskip1pt\underline{\hb@xt@            #1{\hss#2\hss}}\hskip3pt}
    \makeatother

    \begin{minipage}[t]{1.0\linewidth}
        \begin{minipage}[b]{0.65\linewidth}
            \includegraphics[scale=0.15]{logo.jpg}
        \end{minipage}
        \hfill
        \begin{minipage}[b]{0.35\linewidth}
            \begin{flushright}
                \justifying
                {\fontsize{10.5pt}{0}\heiti{
                    \ \\
                    单位代码\dlmu[3cm]{10006}\\
                    学\ \ \ \ \ 号\dlmu[3cm]{38020326}\\
                    分\ 类\ 号\dlmu[3cm]{TN953}\\
                    }}
                \justifying
            \end{flushright}
        \end{minipage}
    \end{minipage}
    \vspace{6.pt}

    \begin{minipage}[th]{0.8\linewidth}
        \centering
            \includegraphics[scale=0.95]{logo1.png}
        \centering
    \end{minipage}
    \vspace{6.pt}
    \\
    \\

    \begin{minipage}[th]{0.9\linewidth}
        \centering
            \maketitle
        \centering
    \end{minipage}
    \vspace{6.pt}
    \\
    \\

    \begin{minipage}[th]{0.9\linewidth}
        \centering
            \title{\fontsize{22pt}{0}\heiti{油/水电迁移微观动态过程的研究}}
        \centering
    \end{minipage}
    \vspace{6.pt}
    \\
    \\
    \\
    \\

    \begin{minipage}[th]{1.0\linewidth}
        \centering
            \justifying
            {\fontsize{15pt}{0}\heiti{
                \ \\
                \ 学\ 院\ 名\ 称\ \dlmu[9cm]{电子信息工程学院}\\
                \ 专\ 业\ 名\ 称\ \dlmu[9cm]{电子与信息技术}\\
                \ 学\ 生\ 姓\ 名\ \dlmu[9cm]{李兴新}\\
                \ 指\ 导\ 教\ 师\ \dlmu[9cm]{毛\ \ \ \ 峡}\\
                }}
            \justifying
        \centering
    \end{minipage}
    \ \\
    \ \\

    \centering
        {\fontsize{15pt}{0}\heiti{2015年\ \ 6月}}
    \centering

\pagestyle{empty}
\thispagestyle{empty}

\end{titlepage}

%---------------------------------------------------------附加一页
%封面书脊
论\\文\\题\\目\\
姓\\名\\
北\\京\\航\\空\\航\\天\\大\\学
\newpage


%之后所有页的页眉设置
\pagestyle{fancy}
\fancyhead[L]{\includegraphics[scale=0.05]{logo.jpg}}
\fancyhead[C]{\fontsize{15pt}{0}\songti{北京航空航天大学毕业设计（论文）}}
\fancyhf[R]{第\ \ \ 页}
\fancyhf[F]{}
\addtolength{\topskip}{7mm}

%---------------------------------------------------------第二页
%摘要部分，包括中文题目、摘要和关键词，以及英文题目、摘要和关键词
\begin{center}
    \title{\fontsize{15pt}{0} \heiti{油/水电迁移微观动态过程的研究}}
\end{center}
\begin{flushright}
    \author{\fontsize{12pt}{0}\songti{学\ \ \ \ \ \ 生：黄\ \ \ 欣\\指导教师：朱岳麟}}
\end{flushright}
\section*{\fontsize{16pt}{0}\heiti {摘\ \ \ \ \ \ 要}}
\begin{paragraph}
    \songti{
    电分离工艺技术在炼油工业中是效率最好、最经济的油/水分离方法。但到目前为止，对于交流、直流或者高频高压条件下，含盐的水珠在油相中电迁移微观动态过程却不十分清楚，因此影响了电脱盐工艺参量的优化。针对这个难题，本文研究了油/水电分离的微观动态过程。建立了一套油/水电迁移显微摄像系统，包括三套电源系统（高频高压电源系统，交流高压电源系统和直流高压电源系统），微电解池系统和显微摄像系统，该装置系统运行稳定可靠，各个部分还可以根据需要组合与调整。运用油/水电迁移显微摄像系统，对油/水体系在高频高压电场中电迁移的微观动态过程进行了探索和研究，总结了油中微水滴在电场中的迁移规律。并分析了高频高压油/水分离的工艺参数对油水电迁移过程的影响，初步确定了油/水分离的最佳频率，以及合适的电场强度。本文将高频高压油/水电迁移动态过程分别与交流高压、直流高压油/水电迁移动态过程进行了对比，分析了其微观机制的不同，验证了高频高压油/水分离技术的优越性。对于油/水电迁移微观机制的研究，不仅为形成完整的油水电分离理论提供了良好的开端，而且对于现有的电脱盐工艺的优化具有重要的指导意义。
    }\\
    \\
\end{paragraph}
    {\fontsize{14pt}{0}\heiti {关键词：}}高频高压、油/水电迁移，微电解池系统，显微摄像系统，微观机制
\newpage
%---------------------------------------------------------第三页
\begin{center}
    {\Large{ Micro-process\ of\ Oil/Water\ Transferring\ in\ Electric\ Field}}
\end{center}

\begin{flushright}
    \author{\fontsize{12pt}{0} {Author : HUANG\ Xin\\Tutor : ZHU Yue-lin}}
\end{flushright}

\section*{\fontsize{16pt}{0} {Abstract \\}}

\begin{paragraph}
    \ Electro-desalting is the most efficient and the most economical oil/water separation method desalting. However the assembling process of water droplet in oil phase under DC、AC and high-frequency high-voltage electric field is not so clear, thus the optimization of crude oil desalting always means a lot of lab work and fieldwork. To resolve thie problem, deep study on the dynamic transferring process of droplets in oil phase was made in this paper. A microcosmic camera apparatus was developed in the research. It includes three power supplies(DC、AC and high-frequency high-voltage powers)、micro-electrolytic cells and microcosmic camera equipments.
\end{paragraph}

\begin{paragraph}
    \ The transfering of water drooplets in oil phase under high-frequency high-voltage electric field has been explored and the rule of the transferring generalized. The effect of such technical parameters as frequency and the most suitable electric field intensity was gained. A contrast of the transferring phenomenon between water droplets ubder different electric fields was performed. The study of the rule of the water droplet transferring in the oil phase made in this paper not only provided a good start for the form of integrate theory of electric separation, but also had a directing effect on the optimizing of existing electro-desalting technics.
\end{paragraph}
\\
\\
{\large {Key words: }}High-frequency high-voltage, Oil/water electro-transferring, Micro-electrolytic cell, Microcosmic camera system

\newpage
%---------------------------------------------------------第四页


\tableofcontents

\newpage
%---------------------------------------------------------第五、六页
\section{绪论}
    \subsection{课题背景及目的}
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子
    \subsection{国内外研究状况}
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子
    \subsection{课题研究方法}
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子
    \subsection{论文构成及研究方法}
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\

\newpage
\section{I 级叶/盘协调转子固有振动特性}
    \subsection{基础知识}
        \subsubsection{有限元法}
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子
        \subsubsection{循环对称结构的分析方法}
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子
    \subsection{I 级叶/盘协调转子振动特性的有限元分析}
        \subsubsection{计算模型}
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子
        \subsubsection{有限元计算结果及分析}
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子
\newpage

\section{I 级叶/盘转子错频方案的对比分析}
在叶轮机械领域，对一个实际的叶盘转子，错频是指由于单个叶片之间因为几何上或结构上的不同而造成的其在固有频率上的差异。$\cdots\cdots$\\
$\cdots\cdots$
    \subsection{计算模型及主要分析思路}
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子
    \subsection{基本原理}
        \subsubsection{多自由度系统的固有频率和振型}
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子
        \subsubsection{多自由度的振动响应}
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子

    \subsection{协调系统的模拟}
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子

    \subsection{错频方案的拟定}
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子\\
    大家好我是小可爱肥兔羔子
    \subsection{多自由度系统的强迫响应分析}
    由前面的分析可知，响应分析在数学上是一个具有38个自由度的二阶线性微分方程的数值积分方程。$\cdots\cdots$
        \subsubsection{动态响应的计算方法}
        1、系统的运动方程\\
        多自由度系统运动微分方程的一般形式为：$\cdots\cdots$\\
        (1)$\cdots\cdots$\\
        (2)$\cdots\cdots$\\

        2、微分方程组的数值积分\\
        一阶常系数微分方程组的初值问题可表述为：$\cdots\cdots$
        \subsubsection{强迫响应分析前的准备工作}
        $\cdots\cdots$
        \subsubsection{动态响应的计算结果与分析}
    \subsection{实际错频方案的动态响应分析}
        \subsubsection{实际错频转子叶片的频率分布}
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子
        \subsubsection{动态响应的计算结果与分析}
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子\\
        大家好我是小可爱肥兔羔子

\addcontentsline{toc}{section}{\ \ \ \ \ \ \ \ \ \ \ \ 结论}

\addcontentsline{toc}{section}{\ \ \ \ \ \ \ \ \ \ \ \ 致谢}

\addcontentsline{toc}{section}{\ \ \ \ \ \ \ \ \ \ \ \ 参考文献}

\addcontentsline{toc}{section}{\ \ \ \ \ \ \ \ \ \ \ \ 附录}

    \addcontentsline{toc}{subsection}{\ \ \ \ \ \ \ \ 附录A}
    \addcontentsline{toc}{subsection}{\ \ \ \ \ \ \ \ 附录B}
    \addcontentsline{toc}{subsection}{\ \ \ \ \ \ \ \ 附录C}
\section*{结论}
\section*{致谢}
\section*{参考文献}
\section*{附录}
计算流体力学（CFD）是一门融合了数学、力学和计算机知识的，以数值求解偏微分方程组为主要内容的学科，广泛应用在工程领域。\\
计算流体力学（CFD）是一门融合了数学、力学和计算机知识的，以数值求解偏微分方程组为主要内容的学科，广泛应用在工程领域。\\
计算流体力学（CFD）是一门融合了数学、力学和计算机知识的，以数值求解偏微分方程组为主要内容的学科，广泛应用在工程领域。\\
计算流体力学（CFD）是一门融合了数学、力学和计算机知识的，以数值求解偏微分方程组为主要内容的学科，广泛应用在工程领域。\\
计算流体力学（CFD）是一门融合了数学、力学和计算机知识的，以数值求解偏微分方程组为主要内容的学科，广泛应用在工程领域。\\
计算流体力学（CFD）是一门融合了数学、力学和计算机知识的，以数值求解偏微分方程组为主要内容的学科，广泛应用在工程领域。\\
计算流体力学（CFD）是一门融合了数学、力学和计算机知识的，以数值求解偏微分方程组为主要内容的学科，广泛应用在工程领域。\\
计算流体力学（CFD）是一门融合了数学、力学和计算机知识的，以数值求解偏微分方程组为主要内容的学科，广泛应用在工程领域。\\
计算流体力学（CFD）是一门融合了数学、力学和计算机知识的，以数值求解偏微分方程组为主要内容的学科，广泛应用在工程领域。\\
计算流体力学（CFD）是一门融合了数学、力学和计算机知识的，以数值求解偏微分方程组为主要内容的学科，广泛应用在工程领域。\\
计算流体力学（CFD）是一门融合了数学、力学和计算机知识的，以数值求解偏微分方程组为主要内容的学科，广泛应用在工程领域。\\
计算流体力学（CFD）是一门融合了数学、力学和计算机知识的，以数值求解偏微分方程组为主要内容的学科，广泛应用在工程领域。\\
计算流体力学（CFD）是一门融合了数学、力学和计算机知识的，以数值求解偏微分方程组为主要内容的学科，广泛应用在工程领域。\\
计算流体力学（CFD）是一门融合了数学、力学和计算机知识的，以数值求解偏微分方程组为主要内容的学科，广泛应用在工程领域。\\
计算流体力学（CFD）是一门融合了数学、力学和计算机知识的，以数值求解偏微分方程组为主要内容的学科，广泛应用在工程领域。\\
计算流体力学（CFD）是一门融合了数学、力学和计算机知识的，以数值求解偏微分方程组为主要内容的学科，广泛应用在工程领域。\\




\end{document}

```

