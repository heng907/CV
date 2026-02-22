\documentclass[10pt, letterpaper]{article}

% Packages:
\usepackage[
    ignoreheadfoot,
    top=1 cm,
    bottom=2 cm,
    left=1.5 cm,
    right=1.5 cm,
    footskip=1.0 cm,
]{geometry}
\usepackage{titlesec}
\usepackage{tabularx}
\usepackage{array}
\usepackage[dvipsnames]{xcolor}
\definecolor{primaryColor}{RGB}{0, 79, 144}
\usepackage{enumitem}
\usepackage{fontawesome5}
\usepackage{amsmath}
\usepackage[
    pdftitle={Yan-Heng,Lin CV},
    pdfauthor={Yan-Heng,Lin},
    pdfcreator={LaTeX with RenderCV},
    colorlinks=true,
    urlcolor=primaryColor
]{hyperref}
\usepackage[pscoord]{eso-pic}
\usepackage{calc}
\usepackage{bookmark}
\usepackage{lastpage}
\usepackage{changepage}
\usepackage{paracol}
\usepackage{ifthen}
\usepackage{needspace}
\usepackage{iftex}

\ifPDFTeX
    \input{glyphtounicode}
    \pdfgentounicode=1
    \usepackage[utf8]{inputenc}
    \usepackage{lmodern}
\fi

% Reduce overall line spacing
\linespread{0.95}

\AtBeginEnvironment{adjustwidth}{\partopsep0pt}
\pagestyle{empty}
\setcounter{secnumdepth}{0}
\setlength{\parindent}{0pt}
\setlength{\topskip}{0pt}
\setlength{\columnsep}{0cm}
\makeatletter
\let\ps@customFooterStyle\ps@plain

\makeatother
\pagestyle{customFooterStyle}

\titleformat{\section}{\needspace{3\baselineskip}\bfseries\large}{}{0pt}{}[\vspace{0.8pt}\titlerule]

\titlespacing{\section}{-1pt}{0.2 cm}{0.15 cm}

\renewcommand\labelitemi{$\circ$}
\newenvironment{highlights}{
    \begin{itemize}[
        topsep=0.05 cm,
        parsep=0.05 cm,
        partopsep=0pt,
        itemsep=0pt,
        leftmargin=0.4 cm + 10pt
    ]
}{
    \end{itemize}
}

\newenvironment{onecolentry}{
    \begin{adjustwidth}{0.2 cm + 0.00001 cm}{0.2 cm + 0.00001 cm}
}{
    \end{adjustwidth}
}

\newenvironment{twocolentry}[2][]{
    \onecolentry
    \def\secondColumn{#2}
    \setcolumnwidth{\fill, 4.5 cm}
    \begin{paracol}{2}
}{
    \switchcolumn \raggedleft \secondColumn
    \end{paracol}
    \endonecolentry
}

\newenvironment{header}{
    \setlength{\topsep}{0pt}\par\kern\topsep\centering\linespread{1.5}
}{
    \par\kern\topsep
}

\newcommand{\placelastupdatedtext}{% \placetextbox{<horizontal pos>}{<vertical pos>}{<stuff>}
  \AddToShipoutPictureFG*{% Add <stuff> to current page foreground
    \put(
        \LenToUnit{\paperwidth-2 cm-0.2 cm+0.05cm},
        \LenToUnit{\paperheight-1.0 cm}
    ){\vtop{{\null}\makebox[0pt][c]{
        \small\color{gray}\textit{Last updated in September 2024}\hspace{\widthof{Last updated in September 2024}}
    }}}%
  }%
}%

% save the original href command in a new command:
\let\hrefWithoutArrow\href

% new command for external links:
\renewcommand{\href}[2]{\hrefWithoutArrow{#1}{\ifthenelse{\equal{#2}{}}{ }{#2 }\raisebox{.15ex}{\footnotesize \faExternalLink*}}}

\hypersetup{
    colorlinks=true,
    allcolors=black,
    urlcolor=black,
    linkcolor=black,
    citecolor=black
}

\begin{document}
    \begin{header}
        \textbf{\fontsize{16 pt}{16 pt}\selectfont Yan-Heng, Lin}

        \vspace{0.1 cm}

        \normalsize
        \mbox{{\color{black}\footnotesize\faMapMarker*}\hspace*{0.13cm}Hsinchu, Taiwan}%
        \kern 0.25 cm%
        \mbox{\hrefWithoutArrow{mailto:yanheng0907@gmail.com}{\color{black}{\footnotesize\faEnvelope[regular]}\hspace*{0.13cm}yanheng0907@gmail.com}}%
        \kern 0.25 cm%
        \mbox{\hrefWithoutArrow{tel:+886-905-158-907}{\color{black}{\footnotesize\faPhone*}\hspace*{0.13cm}+886-905-158-907}}%
        \kern 0.25 cm%
        \mbox{\hrefWithoutArrow{https://github.com/heng907}{\color{black}{\footnotesize\faGithub}\hspace*{0.13cm}heng907}}%
    \end{header}

    \vspace{0.1 cm}
% Education
    \section{Education}
        \begin{twocolentry}{
        \textit{Jul. 2022 – Present}}
            \textbf{National Yang Ming Chiao Tung University, Hsinchu, Taiwan}
        \end{twocolentry}
        \vspace{0.10 cm}
        \begin{onecolentry}
            \begin{highlights}
                \item Major in Computer Science
                \item Core Courses: \href{https://github.com/heng907/NYCU-coursework.git}{Link}
            \end{highlights}
        \end{onecolentry}
% Experience
    \section{Experience}
        \begin{itemize}[leftmargin=0.4cm]
            \item
                \begin{twocolentry}{\textit{Sep. 2024 - Jun. 2025}}
                    \textbf{Undergraduate Researcher | ESSLab}
                \end{twocolentry}
                \begin{highlights}
                    \item Developed an energy-aware inference strategy using Early Exit Neural Networks (EENN) for memory-constrained EH devices.
                    \item Optimized system sustainability under unstable power supply, maintaining a consistent 80\% inference accuracy.
                \end{highlights}
                \vspace{-0.2cm}


            
        \end{itemize}
% Projects
    \section{Projects}

        \begin{twocolentry}{
        \textit{\href{https://github.com/heng907/2024-AI-Final-Project.git}{Link}}}
            \textbf{Text Sentiment Analysis System} 
        \end{twocolentry}
        \vspace{0.05 cm}
        \begin{onecolentry}
            \begin{highlights}
                \item Developed a sentiment analysis model capable of predicting the sentiment of a given text
                \item Enhanced model to manage real-world Out-of-Vocabulary (OOV) words through Data Augmentation. 
                \item Tool Used: Python, Kaggle
            \end{highlights}
        \end{onecolentry}

        \begin{twocolentry}{
        \textit{\href{https://github.com/heng907/Cryptography-Engineering.git}{Link}}}
            \textbf{Homomorphic encryption on Machine Learning} 
        \end{twocolentry}
        \vspace{0.05 cm}
        \begin{onecolentry}
            \begin{highlights}
                \item Developed a secure ML pipeline that enables model training and inference directly on encrypted data, ensuring end-to-end data privacy.
                \item Designed a Client-Server architecture where the server processes encrypted datasets from the client without ever accessing raw sensitive information.
                \item Tool Used: Python
            \end{highlights}
        \end{onecolentry}

        \begin{twocolentry}{
        \textit{\href{https://github.com/heng907/ML-final-project.git}{Link}}}
            \textbf{Identification of Human (real) VS. AI-generated images} 
        \end{twocolentry}
        \vspace{0.05 cm}
        \begin{onecolentry}
            \begin{highlights}
                \item Implemented with ResNet50-based binary classifier with ImageNet-pretrained weights reaching an 
                \item Applied Transfer Learning, ColorJitter augmentation, and Cosine Annealing to maximize model generalization and accuracy.
                \item Tool Used: Python, Kaggle, PyTorch
            \end{highlights}
        \end{onecolentry}


        \begin{twocolentry}{
        \textit{\href{https://github.com/heng907/CA-final-project.git}{Link}}}
            \textbf{Investigating Implicit Inverse Kinematics in LGTM Diffusion Model} 
        \end{twocolentry}
        \vspace{0.05 cm}
        \begin{onecolentry}
            \begin{highlights}
                \item Implemented a hierarchical motion diffusion model (LGTM) capable of generating cohesive 3D human animations from natural language prompts.
                \item Analyzed the impact of prompt engineering on motion synthesis, comparing IK-like (spatial constraints) vs. FK-like (joint-based) descriptions to optimize semantic alignment.
                \item Tool Used: Python, PyTorch, fmbvh
            \end{highlights}
        \end{onecolentry}

        \begin{twocolentry}{
        \textit{\href{https://github.com/heng907/FinalProject.git}{Link}}}
            \textbf{Film Filter} 
        \end{twocolentry}
        \vspace{0.05 cm}
        \begin{onecolentry}
            \begin{highlights}
                \item Develop a comprehensive movie review website.
                \item Users to filter shows based on specific criteria. The Web page let users provide ratings and fostering a vibrant community passionate about sharing and discovering diverse cinematic experiences on our it.
                \item Tool Used: Python, JavaScript, HTML, Django, Git
            \end{highlights}
        \end{onecolentry}



        

% Skills

    \section{Skills}
        \begin{onecolentry}
            \textbf{Languages:} C++, C, Python, JavaScript, SQL, Shell Script
        \end{onecolentry}
        
        \vspace{0.15 cm}
        \begin{onecolentry}
            \textbf{Framework:} Vue, Django
        \end{onecolentry}
        
        \vspace{0.15 cm}
        \begin{onecolentry}
            \textbf{Techniques:} Image Processing, Network \& System Administration, Operating System
            
        \end{onecolentry}

        \vspace{0.15 cm}
        \begin{onecolentry}
            \textbf{Tools:} PyTorch, OpenCV, Docker, Git, Linux, FreeBSD, Ubuntu

        \end{onecolentry}
% Awards
    \section{Awards}
        \vspace{0.15 cm}
        \begin{twocolentry}{\textit{Nov. 2024}}
                \textbf{2nd Place} | 2024 Meichu Hackathon
        \end{twocolentry}
        \vspace{0.15 cm}
        \begin{twocolentry}{\textit{Nov. 2023}}
                \textbf{3rd Place} | 2023 Meichu Hackathon
        \end{twocolentry}
% Extracurricular Activities

    \section{Extracurricular Activities}

        \begin{twocolentry}{\textit{Jun. 2023 - Jun. 2024}}
                \textbf{Member} | NYCU Computer Science Student Association 2023
        \end{twocolentry}

\end{document}