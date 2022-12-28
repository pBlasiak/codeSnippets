Code snippets for LaTeX
========================================


LaTeX
------------

- [Tables with footnote](#tables-with-footnote)
- [Figures with caption and subcaptions](#figures-with-caption-and-subcaptions)
- [Listing](#listing)


## Tables with footnote

	\begin{table}[H]
	\begin{threeparttable}[b]
	\centering
	\caption{<++>}
		\begin{tabular}{cccp{5.865em}ccc}
		\toprule
		    	      & \multicolumn{3}{c}{TI = 5\%} & \multicolumn{3}{c}{TI = 10\%}                                                                 \\
		    	      & dp                           & Tmax  & \multicolumn{1}{c}{Remark} & dp    & Tmax  & Remark                                   \\
					\midrule
		    	\multicolumn{1}{p{9em}}{Model turbulencji} & [Pa]  & [K]   & \multicolumn{1}{c}{} & [Pa]  & [K]   &                                  \\
		    	\midrule
		    	LRR            & -     & -       & \multicolumn{1}{c}{Lack of R} & -     & -       & -                                                \\
				LamBremhorstKE & 12516 & 1,73291 & Divergence\tnote{1}           & 13316 & 1,73542 & \multicolumn{1}{p{7.955em}}{Divergence\tnote{1}} \\
	   	\bottomrule
	   	\end{tabular}%
	\label{tab:<++>}%
	
	\begin{tablenotes}
	   \item [1] $T>2.17$ K after 1 s when the heater was turned on
	\end{tablenotes}
	
	\end{threeparttable}
	\end{table}

## Figures with caption and subcaptions


	\begin{figure}[H]
	\centering
	\subfloat[<++>]{\includegraphics[scale=0.28]{figures/<++>}\label{fig:<++>}}
	  \\
	\subfloat[<++>]{\includegraphics[scale=0.28]{figures/<++>}\label{fig:<++>}}
	
	\caption{<++>} 
	\label{fig:<++>}
	\end{figure}


## Listing

	\begin{lstlisting}[language=C++, label=lst:<++>, caption=<++>]
		<++>
	\end{lstlisting}


