# latex_utilities


Usage example:
```latex
% ...

%----------------------------------------------------------------------------------------
%   File settings
%----------------------------------------------------------------------------------------

% Load all required basic packages
\input{utilities/basic}
\input{utilities/commands}

% Bad boxes settings and programming environments
\input{utilities/badboxes}
\input{utilities/programming}

% Input a empty list of commands when on debug mode
\input{utilities/commands_list}

% ...
```


Full example:
```latex
%
% Licensing
%
%   Copyright 2017 @ Student
%
%  This program is free software; you can redistribute it and/or modify it
%  under the terms of the GNU General Public License as published by the
%  Free Software Foundation; either version 3 of the License, or ( at
%  your option ) any later version.
%
%  This program is distributed in the hope that it will be useful, but
%  WITHOUT ANY WARRANTY; without even the implied warranty of
%  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU
%  General Public License for more details.
%
%  You should have received a copy of the GNU General Public License
%  along with this program.  If not, see <http://www.gnu.org/licenses/>.
%

%
% Simple Sectioned Essay Template - LaTeX Template
%
% This template has been downloaded from:
% http://www.latextemplates.com
%
% `proposal.tex`
% Based on http://www.latextemplates.com/template/simple-sectioned-essay
%


%----------------------------------------------------------------------------------------
%   PACKAGES AND OTHER DOCUMENT CONFIGURATIONS
%----------------------------------------------------------------------------------------

% Sets this document font size to 12pt and set is type to article
\documentclass[12pt]{article}

% Will allow all displayable utf8 characters to be available as input
% https://tex.stackexchange.com/questions/13067/utf8x-vs-utf8-inputenc
% https://tex.stackexchange.com/questions/664/why-should-i-use-usepackaget1fontenc
\usepackage[T1]{fontenc}
\usepackage[utf8]{inputenc}

% Sets this document language usage to Portuguese
\usepackage[brazil]{babel}

% Set the page size to be A4 as opposed to the default US Letter
\usepackage[a4paper, margin=2cm]{geometry}


%----------------------------------------------------------------------------------------
%   File settings
%----------------------------------------------------------------------------------------

% Load all required basic packages
\input{utilities/basic}
\input{utilities/commands}

% Bad boxes settings and programming environments
\input{utilities/badboxes}
\input{utilities/programming}

% Input a empty list of commands when on debug mode
\input{utilities/commands_list}

% To use the font Times New Roman, instead of the default LaTeX font
% \usepackage{mathptmx}
%
% more up-to-date than 'mathptmx'
\usepackage{newtxtext,newtxmath}

% https://tex.stackexchange.com/questions/10377/texttt-overfull-hbox-problem
% https://tex.stackexchange.com/questions/66052/should-i-load-microtype-with-pdflatex
\usepackage{microtype}

% Indent the first section paragraphs
% https://tex.stackexchange.com/q/39227/119062
\usepackage{indentfirst}

% Why is the linespread factor as it is?
% \linespread{1.5}
% https://tex.stackexchange.com/questions/30073/why-is-the-linespread-factor-as-it-is
\usepackage{setspace}

% \doublespacing
\onehalfspacing

% Specifies the directory where pictures are stored
\graphicspath{{pictures/}}
```



## Begin document alternative 1
```
%----------------------------------------------------------------------------------------
%   DOCUMENT CONTENTS
%----------------------------------------------------------------------------------------

\begin{document}

    \Title{Answers}

    University Coo - TTR - FAP4401 - Programming 1

    Student: ...

    City, \today.


\tableofcontents
\addGoToSummary
\newpage

\section{Introdução}

   % ...


\include{implementation}
% ...


\end{document}
```


## Begin document alternative 2
```latex
%----------------------------------------------------------------------------------------
%   DOCUMENT CONTENTS
%----------------------------------------------------------------------------------------

\begin{document}

% pdfTeX warning (ext4): destination with the same identifier (nam e{page.1}) has been already used
% https://tex.stackexchange.com/questions/18924/
\hypersetup{pageanchor=false}

% Author name
%
% What do \makeatletter and \makeatother do?
% https://tex.stackexchange.com/questions/8351/what-do-makeatletter-and-makeatother-do
%
% How can I use @author, @date, and @title after maketitle?
% https://tex.stackexchange.com/questions/27710/how-can-i-use-author-date-and-title-after-maketitle
\makeatletter
\author{Student}\let\Author\@author

% \author{Someone}          \let\Author\@author
% \date{Somewhen}           \let\Date\@date
\def\Advisor{Person A}
\def\Supervisor{B Person}
\makeatother

\include{cover}
\include{abstract}
\include{summary}

% To automatically put a [Go To Top] on each section
\addGoToSummary

\include{introduction}
\include{schedule}
% ...

\bibliographystyle{abbrv}
\bibliography{refs}

\end{document}
```


# License

```latex
%% README.md
%% Copyright 2017 Evandro Coan
%
% This work may be distributed and/or modified under the
% conditions of the LaTeX Project Public License, either version 1.3
% of this license or (at your option) any later version.
% The latest version of this license is in
%   http://www.latex-project.org/lppl.txt
% and version 1.3 or later is part of all distributions of LaTeX
% version 2005/12/01 or later.
%
% This work has the LPPL maintenance status `maintained'.
%
% The Current Maintainer of this work is M. Y. Name.
%
% This work consists of the files `README.md`, `basic.tex`,
% `commands.tex` and `programming.tex`.
```

