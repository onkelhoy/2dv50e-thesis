
\subsection{Permutation Experiments}

The permutation setup utilizes the \texttt{itertools} library in Python, leveraging its permutations function which accepts two arguments: \texttt{list} and \texttt{radius}. Here, \texttt{list} refers to a predefined list of algorithms (each with specific parameters), and \texttt{radius} specifies the desired size of the layer, denoted by $\min(|\texttt{list}|, r)$ with a default value of 3. This produces a sequence of algorithm permutations that are fed into the \texttt{Layer} class to construct the architecture.

These permutations are generated within the \texttt{experiment} function located in the \texttt{permutation} module, designed to facilitate experiment execution. This function accepts several parameters:

\begin{enumerate}
    \item \textbf{dataset}: A JSON object containing \texttt{paths}, an array of image URLs.
    \item \textbf{layer\_size}: The radius for the permutation function.
    \item \textbf{dataset\_size}: The number of image paths processed by the Layer.
    \item \textbf{config}: Configuration array, detailing each algorithm and its parameters. If set to \textit{"all"}, it uses the \texttt{presets} array instead.
    \item \textbf{presets}: Predefined settings for algorithms, facilitating rapid setup.
    \item \textbf{accuracy\_calculator}: Function to compute accuracy; defaults to a built-in method if none is specified.
    \item \textbf{foldername}: Destination subdirectory within the 'outputs' directory for saving results.
\end{enumerate}

Results are evaluated using the \texttt{accuracy\_calculator} function and include scores and algorithm performance metrics, which are stored alongside raw results in the designated output folder.

\subsection{Manual Parameter Tuning}

Users are responsible for manually adjusting algorithm parameters to optimize performance criteria such as speed and accuracy. These customized settings are then passed to the \texttt{experiment} function either as \texttt{config} or \texttt{presets}.
