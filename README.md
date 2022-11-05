Code snippets for LaTeX and Bash
========================================


LaTex
------------

- Tables with footnote

&nbsp;


	\begin{table}[H]
		\begin{threeparttable}[b]
	  \centering
	  \caption{The results of $\Delta p$ and $T_{max}$ for transient case of 16 m/s
	  with $T_{out}=1.7$ K, nonuniform mesh and for different turbulence intensities and
	  turbulence models}
	    \begin{tabular}{cccp{5.865em}ccc}
			\toprule
	          & \multicolumn{3}{c}{TI = 5\%} & \multicolumn{3}{c}{TI = 10\%} \\
	          & dp    & Tmax  & \multicolumn{1}{c}{Remark} & dp    & Tmax  & Remark \\
	    \midrule
	    \multicolumn{1}{p{9em}}{Model turbulencji} & [Pa]  & [K]   & \multicolumn{1}{c}{} & [Pa]  & [K]   &  \\
	    \midrule
	    LRR   & -     & -     & \multicolumn{1}{c}{Lack of R} & -     & -     & - \\
		LamBremhorstKE & 12516 & 1,73291 & Divergence\tnote{1} & 13316 & 1,73542 & \multicolumn{1}{p{7.955em}}{Divergence\tnote{1}} \\
		LaunderSharmaKE & 12363 & 1,73172 & Divergence\tnote{1} & 13173 & 1,73291 & \multicolumn{1}{p{7.955em}}{Divergence\tnote{1}} \\
	    LienCubicKE & 11632 & > 2,17 & Divergence & 12140 & > 2,17 & Divergence \\
		LienLeschziner & 12516 & 1,73172 & Divergence\tnote{1} & 13369 & 1,73542 & Divergence \\
		RNGkEpsilon & 11428 & 1,72815 & Divergence\tnote{1} & 12554 & 1,73291 & \multicolumn{1}{p{7.955em}}{Divergence\tnote{1}} \\
	    SSG   & -     & -     & \multicolumn{1}{c}{Lack of R} & -     & -     & - \\
	    ShihQuadraticKE & 10862 & > 2,17 & Divergence & 12192 & > 2,17 & Divergence \\
	    SpalartAlmaras & 145   & 1,7002 & Converged & 145   & 1,7002 & Converged \\
		k-e   & 12554 & 1,73291 & Divergence\tnote{1} & 13268 & 1,73661 & Divergence\tnote{1} \\
		kEpsilonLopesdaCosta & 12554 & 1,73172 & Divergence\tnote{1} & 13316 & 1,73661 & Divergence\tnote{1} \\
	    kEpsilonPhitF & -     & -     & Lack of phit & -     & -     & Lack of phit \\
		kOmega & 13184 & 1,73291 & \multicolumn{1}{c}{} & 13715 & 1,7378 & Divergence\tnote{1} \\
	    kOmeaSST & 12159 & > 2,17  & Divergence & 12580 & > 2,17 & Divergence \\
	    kOmegaSSTLM & -     & -     & Lack of ReThetat & -     & -     & Lack of ReThetat \\
	    kOmegaSSTSAS & -     & -     & Lack of delta. & -     & -     & Lack of delta. \\
	    kkLOmega & -     & -     & Lack of kt & -     & -     & Lack of kt \\
	    qZeta & 13489 & > 2,17 & Divergence & 13993 & > 2,17 & Divergence \\
	    realizableKE & 11484 & 1,72747 & Calculating & 12040 & 1,72934 & Divergence \\
	    \bottomrule
	    \end{tabular}%
	  \label{tab:turbModelImpactOnDp}%
	  \begin{tablenotes}
	  \item [1] $T>2.17$ K after 1 s when the heater was turned on
	     \end{tablenotes}
	    \end{threeparttable}

- Figures with caption and subcaptions


&nbsp;





Bash
------------

- Usuniecie wszystkich linii w pliku zawierajacych znaki "step"

&nbsp;

	sed -i '/step/d' nazwaPliku
