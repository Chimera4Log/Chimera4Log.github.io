---
layout: project_page
permalink: /

title: "United We Stand: Towards End-to-End Log-based Fault Diagnosis via Interactive Multi-Task Learning"

authors: |
    Anonymous Submission

code: |
    https://anonymous.4open.science/r/Chimera
# video: |
#     https://youtu.be/IFFLb5mgzY0
---

<!-- 
# paper: https://www.cs.virginia.edu/~robins/Turing_Paper_1936.pdf
#  <span>^1^Microsoft,</span> <span>^2^Institute of Automation, Chinese Academy of Sciences,</span> <span>^3^School of Artificial Intelligence, University of Chinese Academy of Sciences,</span>
    # Microsoft
    # Institute of Automation, Chinese Academy of Sciences
    # School of Artificial Intelligence, University of Chinese Academy of Sciences
# paper: 'coming soon'
# video: https://www.youtube.com/results?search_query=turing+machine
# code: 'coming soon'
# data: https://huggingface.co/docs/datasets
 -->

<!-- <video width="100%" height="auto" controls>
  <source src="{{ site.baseurl }}/static/video/AutoRAG.mp4" type="video/mp4">
</video> -->

---

<!-- Using HTML to center the abstract -->
<div class="columns is-centered has-text-centered">
    <div class="column is-four-fifths">
        <h2>Abstract</h2>
        <div class="content has-text-justified">
Log-based fault diagnosis is essential for maintaining software system availability. However, existing fault diagnosis methods are built using a task-independent manner, which fails to bridge the gap between anomaly detection and root cause localization in terms of data form and diagnostic objectives, resulting in three major issues: 1) Diagnostic bias accumulates in the system; 2) System deployment relies on expensive monitoring data; 3) The collaborative relationship between diagnostic tasks is overlooked. Facing this problems, we propose a novel end-to-end log-based fault diagnosis method, Chimera, whose key idea is to achieve end-to-end fault diagnosis through bidirectional interaction and knowledge transfer between anomaly detection and root cause localization. Chimera is based on interactive multi-task learning, carefully designing interaction strategies between anomaly detection and root cause localization at the data, feature, and diagnostic result levels, thereby achieving both sub-tasks interactively within a unified end-to-end framework. Evaluation on two public datasets and one industrial dataset shows that Chimera outperforms existing methods in both anomaly detection and root cause localization, achieving improvements of over 2.92%~5.00% and 19.01%~37.09%, respectively. It has been successfully deployed in production, serving an industrial cloud platform.
        </div>
    </div>
</div>



<!-- > Note: This is an example of a Jekyll-based project website template: [Github link](https://github.com/shunzh/project_website).\
> The following content is generated by ChatGPT. The figure is manually added. -->

## Key Contributions
1. We proposed an end-to-end log-based fault diagnosis system, Chimera, which achieves anomaly detection and root cause localization interactively within a unified framework through carefully designed interaction strategies.

2.  We designed a sequence-driven localizer based on the principle of multiple-instance learning, which utilizes only anomalous log sequences for training without the need for root cause logs.

3.  We proposed a multi-task interaction strategy based on disentanglement learning and mutual information theory, which facilitates interaction at the feature and diagnostic result levels, effectively promoting knowledge transfer between tasks.

4.  Evaluations on two public datasets and one industrial dataset demonstrate the significant effectiveness of our approach.

## Main Ideas
<div align="center">
    <img src= "{{ site.baseurl }}/static/image/teaser.jpg" alt="Hierarchical UCB" style="width: 60%;">
    <p><em>Figure 1: Two different fault diagnosis deployment paradigms. The existing log-based fault diagnosis method is deployed in a task-independent paradigm. Initially, the labeled log sequences and log entries are inputted, and the detector and localizer are trained independently. Finally, the two are integrated into a fault diagnosis network, leading to issues such as diagnostic bias accumulates. The proposed log-based fault diagnosis method is deployed in an task-interactive paradigm. The labeled log sequence is used to train the detector and localizer interactively in an end-to-end manner, resulting in excellent diagnostic performance.</em></p>
</div>

<br><br> <!-- Adding two extra empty lines -->

<div align="center">
    <img src= "{{ site.baseurl }}/static/image/pipeline.jpg" alt="Hierarchical UCB" style="width: 150%; display: block; margin-left: auto; margin-right: auto;">
    <p><em>Figure 2: The proposed end-to-end log-based fault diagnosis pipeline for Chimera. Chimera pipeline comprises three key stages: Log Preprocessing, Interactive Log Representation Learning (ILRL), and Joint Fault Diagnosis. Firstly, the raw system logs are labeled and parsed into log event sequences, and corresponding log embeddings are extracted. Secondly, the ILRL module to learns shared and private representations for anomaly detection and root cause localization interactively, and combines them into a log representation for fault diagnosis. Finally, the learned log representation is fed into the localizer and detector for joint fault diagnosis. Chimera bridges the gap between anomaly detection and root cause localization through their bidirectional interaction and knowledge transfer, achieving more effective end-to-end fault diagnosis.</em></p>
</div>

<br><br> <!-- Adding two extra empty lines -->

<div align="center">
    <img src= "{{ site.baseurl }}/static/image/workflow.jpg" alt="Hierarchical UCB" style="width: 150%; display: block; margin-left: auto; margin-right: auto;">
    <p><em>Figure 3: The workflow of Sequence-driven Localizer. Given embeddings of log sequence, the network outputs a score for each log and locates the root cause log. The localizer is designed based on the principle of multi-instance learning, and locates the root cause log by comparing the scores of normal log sequences and anomalous log sequences.</em></p>
</div>

<!-- ## Table: Comparison of Computable and Non-Computable Numbers

| Computable Numbers | Non-Computable Numbers |
|-------------------|-----------------------|
| Rational numbers, e.g., 1/2, 3/4 | Transcendental numbers, e.g., π, e |
| Algebraic numbers, e.g., √2, ∛3 | Non-algebraic numbers, e.g., √2 + √3 |
| Numbers with finite decimal representations | Numbers with infinite, non-repeating decimal representations |

He used the concept of a universal Turing machine to prove that the set of computable functions is recursively enumerable, meaning it can be listed by an algorithm. -->
<!-- 
## Significance
Turing's paper laid the foundation for the theory of computation and had a profound impact on the development of computer science. The Turing machine became a fundamental concept in theoretical computer science, serving as a theoretical model for studying the limits and capabilities of computation. Turing's work also influenced the development of programming languages, algorithms, and the design of modern computers. -->

