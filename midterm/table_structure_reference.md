
\begin{table}[H]
\centering
\scriptsize  % Reduce font size for compactness
\caption{Comparative Analysis of Methodological Approaches: Similarities}
\label{tab:similarities}
\renewcommand{\arraystretch}{7} % Adjust row spacing if needed
\begin{tabular}{p{0.4cm}p{2.8cm}p{4.0cm}}
\hline
\textbf{Ref.} & \textbf{Approach} & \textbf{Similarities} \\
\hline
\textbf{\cite{xiao2021}} 
  & Direction-dominated Change Vector Analysis \cite{xiao2021}  & The analysis of direction change vectors plays a crucial role in this study as it requires threshold calibration to distinguish genuine change from noise in which is necessary for the remaining studies. \\[1mm]
\textbf{\cite{amatya2021}} 
  & Object-based Image Analysis \cite{amatya2021} 
  & Object-based Image analysis heavily relies on segmentation and object-delineation which emphasizes parameter tuning for optimal detection, similar to that of the calibration needs in other methods. \\[1mm]
\textbf{\cite{ye2021}} 
  & Landsat Time Series: Stochastic Continuous Change Detection \cite{ye2021}
  & Some studies implements a time-series approach for real-time monitoring due to the need for threshold setting and sensitivity adjustment to manage natural variability. \\[1mm]
\textbf{\cite{hassan2022}} 
  & Weighted Mean of Vectors Algorithm \cite{hassan2022} 
  & Makes use of an algorithm as a weighting mechanism to enhance signal importance which adds a layer of threshold and sensitivity similarly to the other studies. \\[1mm]
\textbf{\cite{giannetti2021}} 
  & Time series Sentinel-2 imagery and Continuous Change Detection Algorithms \cite{giannetti2021}
  & Time series usually focuses on continuous monitoring using certain data in which this similarly demands calibration to handle subtle spectral variations and ensure reliable detection. \\
\hline
\end{tabular}
\end{table}

\FloatBarrier

\hyperref[tab:similarities]{Table I} mentioned the similarities among various methodological approaches used in recent remote sensing studies. The specific approaches may vary, however they all collectively signify the importance of change vector analysis in terms of remote sensing through highlighting their shared reliance on threshold calibration, segmentation/parameter tuning, and sensitivity adjustments. Despite differing in implementation and application focus, these approaches all emphasize the need to fine-tune detection parameters to reliably distinguish genuine changes from noise, thereby ensuring accurate and robust monitoring of forest disturbances.

\FloatBarrier 

\begin{table}[H]
    \caption{Summary of 5 Journal Papers}
    \centering
    \renewcommand{\arraystretch}{2}
    \large
    \resizebox{\columnwidth}{!}{
    \begin{tabular}{p{3cm} p{5cm} p{2.5cm} p{4cm}} 
        \hline
        \textbf{Paper Title} & \textbf{Focus} & \textbf{Mathematical Tools Used} & \textbf{Key Findings} \\
        \hline
        Landslide Mapping Using Object-Based Image Analysis and Open Source Tools \cite{amatya2021}  
        & Selecting and tuning segmentation parameters in OBIA. Landslides vary in size, shape, and spectral characteristics; coarse settings merge features with the background, while fine settings lead to over-segmentation. 
        & Plateau Objective Function (POF), topographic indices with multi-temporal data. 
        & Improved delineation accuracy and reduced misclassification between landslides and stable terrain. \\
        
        A Near-Real-Time Approach for Monitoring Forest Disturbance Using Landsat Time Series: Stochastic Continuous Change Detection \cite{ye2021}  
        & Achieving the right balance between sensitivity and specificity. The algorithm must detect genuine disturbances early without triggering false alarms from noise, cloud cover, and seasonal variations. 
        & Threshold selection via time-adaptive thresholding, structural time-series models with a Kalman filter. 
        & Enhanced detection reliability that distinguishes genuine disturbances from transient spectral fluctuations. \\
        
        Evaluation of Weighted Mean of Vectors Algorithm for Identification of Solar Cell Parameters \cite{hassan2022}  
        & Tuning parameter boundaries and designing an effective fitness function for a complex, high-dimensional, nonlinear search space with multiple local optima and noisy measurement data. 
        & Wavelet-based weighted mean. 
        & Improved convergence accuracy and efficient parameter estimation in complex optimization tasks. \\
        
        Direction-Dominated Change Vector Analysis for Forest Change Detection \cite{xiao2021}  
        & Determining an optimal global magnitude threshold to differentiate genuine forest changes from background variability, compounded by the challenge of selecting appropriate spectral bands from Sentinel-2A data. 
        & Expectation-Maximization (EM) algorithm , spatial filtering, confidence-weighted reclassification, k-means clustering. 
        & Enhanced change detection accuracy with reduced false positives and improved differentiation of forest disturbance types. \\
        
        Estimating VAIA Windstorm Damaged Forest Area in Italy Using Time Series Sentinel-2 Imagery and Continuous Change Detection Algorithms \cite{giannetti2021}  
        & Calibrating detection thresholds to identify subtle windstorm-induced damage while mitigating interference from natural variability, seasonal changes, and atmospheric effects. 
        & Probability-based stratified estimators, multi-seasonal trend analysis, Cohen’s Kappa assessment. 
        & More reliable damage detection with increased confidence in damage area estimates and reduced impact of seasonal variability. \\
        \hline
    \end{tabular}
    }
    \label{tab:summaryjournal}
\end{table}


\FloatBarrier

\hyperref[tab:summaryjournal]{Table II} presents a comparative summary of five journal papers, each addressing different challenges in remote sensing, optimization, and change detection. While the specific focus of each study varies, they collectively emphasize advancements in algorithmic methodologies for analyzing geospatial and environmental data.  

Despite employing distinct mathematical tools—ranging from probabilistic modeling and time-series analysis to adaptive thresholding and machine learning—the studies share a common objective: improving the accuracy and reliability of automated detection and classification systems. These shared methodologies highlight the broader significance of structured analytical approaches in remote sensing, optimization, and environmental monitoring.  


\FloatBarrier

\section{Challenges and Issues}

Challenges arise at multiple stages when using object-based image analysis (OBIA) and open-source tools for landslide detection . The primary challenge is the selection and tuning of segmentation parameters within the object-based image analysis (OBIA) framework \cite{amatya2021}. Since landslides vary greatly in size, shape, and spectral characteristics, identifying the optimal range radius and minimum object size is critical. If the parameters are set too coarsely, distinct landslide features may be merged with the background; if set too finely, the resulting segmentation may become overly fragmented, complicating subsequent object merging and classification. This delicate balance in parameter calibration is essential to ensure that the OBIA approach can reliably delineate landslide boundaries using open-source tools.

A near-real-time monitoring system  for forest disturbance detection using Landsat time series and a stochastic continuous change detection framework \cite{ye2021} has the main challenge that they are addressing is achieving the right balance between sensitivity and specificity: the algorithm must be sensitive enough to detect genuine disturbances early, yet robust enough to avoid excessive false alarms caused by inherent noise, cloud cover, seasonal variability, and other transient fluctuations in the data. This delicate trade-off requires careful calibration of detection thresholds and model parameters so that the stochastic framework can reliably distinguish significant changes from benign variations in the reflectance time series.

The implementation of the weighted mean from vectors algorithm (INFO) faces several issues. The definition of parameter boundaries and the design of the fitness function set the framework for the optimization process. Its main challenge \cite{hassan2022}  is optimally tuning the weighted mean of vectors algorithm to reliably estimate solar cell parameters. This involves selecting the appropriate parameter boundaries, scaling factors, and fitness function settings so that the algorithm can navigate a complex, high-dimensional search space with nonlinear behavior and multiple local optima, all while avoiding premature convergence and handling noisy measurement data.

A direction-dominated change vector analysis (DCVA) method presents challenges~\cite{xiao2021}. the main challenge lies in determining an optimal global magnitude threshold to distinguish genuine forest changes from background variability. If the threshold is set too low, the method tends to generate false positives by misinterpreting minor spectral variations or noise as change. Conversely, setting it too high risks missing subtle but important disturbances in forest cover.   The selection of appropriate spectral bands from Sentinel-2A data, which do not all contribute equally to change detection, further complicates implementation~\cite{xiao2021}.

Applying continuous change detection algorithms (BFAST and CCDC) for mapping windstorm‐damaged forest areas presents challenges~\cite{giannetti2021}.  Calibrating the continuous change detection algorithm to reliably identify windstorm-induced forest damage and this task is particularly difficult because the spectral signals of damage can be subtle and are often confounded by natural variability, seasonal changes, and atmospheric effects. Additionally, setting appropriate thresholds to differentiate between genuine damage and transient noise (e.g., due to clouds or illumination differences) is critical—too low a threshold may lead to false positives, while too high a threshold risks missing significant damage. Overcoming these challenges requires a careful balance of sensitivity and specificity, as well as robust preprocessing of the time series Sentinel-2 imagery to minimize interference from extraneous factors.