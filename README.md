---
number: 28 # leave as-is, maintainers will adjust
title: The Impact of Dataset Size on Bayesian Optimization, Insights from the QM9 Dataset
topic: benchmark-task
team_leads:
  - Jose Manuel Napoles Duarte (Autonomous University of Chihuahua)

# Comment these lines by prepending the pound symbol (#) to each line to hide these elements
contributors:
  - Erick Lopez Saldivar (Autonomous University of Chihuahua) @SilkenMocha
  - Christian Emmanuel Granados Cervantes (Autonomous University of Chihuahua) @Salario-Minimo
  - Anthony Onwuli (Imperial College London) @AntObi
  - Xuan Vu Nguyen (Università degli Studi di Milano Statale) @XuanVuNguyen

github: AC-BO-Hackathon/Chihuahuas
# youtube_video: <your-video-id>
---


The "Chihuahuas" team's research focuses on establishing the critical threshold of dataset size for achieving reliable results 
with Bayesian optimization for the QM9 dataset. Our study aims to discern the minimum dataset volume necessary for dependable 
optimization outcomes, a question of paramount importance in fields where data may be scarce or costly to acquire. By systematically
examining how Bayesian optimization performs across varying dataset sizes we intend to offer insights into the optimal use of limited 
data resources. This endeavor is crucial for maximizing the efficacy of computational methods in scenarios where the dataset size is 
constrained, ensuring that Bayesian optimization remains a viable and effective tool for advancing research and applications in 
deep learning for chemistry and beyond.

[![IMAGE ALT TEXT HERE]([https://github.com/AC-BO-Hackathon/Chihuahuas/blob/main/youtube.png](https://www.youtube.com/watch?v=hvODyYejxuc)

# Introduction:

The primary purpose of this research is to investigate the efficacy of Bayesian Optimization (BO) in tuning hyperparameters of Graph Convolutional Neural Networks (GCNNs) across datasets of varying sizes from the QM9 dataset, focusing on parameters such as learning rate, batch size, and number of neurons. This study is driven by the challenge of optimizing machine learning models in the context of limited data availability—a common scenario in the fields of chemistry and materials science. By systematically exploring the impact of dataset size on the BO process, the research aims to:

Determine the Minimum Viable Dataset Size: Identify the smallest dataset size that allows for the effective application of BO to tune the GCNN hyperparameters, providing valuable insights into the feasibility of applying machine learning techniques to small datasets in computational chemistry.

Optimize Model Performance: Through the optimization of critical hyperparameters, enhance the accuracy and efficiency of GCNN models in predicting molecular properties, thereby contributing to more efficient computational experiments and the potential discovery of novel materials.

Provide a Methodological Blueprint: Offer a comprehensive framework for applying BO in scenarios where data is scarce, including guidelines for selecting hyperparameters and adjusting optimization strategies based on dataset size.

Address the Challenges of Data Scarcity: By demonstrating the applicability of BO to smaller datasets, this research addresses a significant barrier in computational chemistry and materials science, paving the way for the advancement of research even when large datasets are not available.

Ultimately, this research seeks to bridge the gap between the potential of machine learning in theoretical chemistry and the practical limitations posed by data availability, fostering innovation and discovery in the field.

Code:

You can see the code for optimizing:

1) [Learning rate](https://github.com/AC-BO-Hackathon/Chihuahuas/blob/main/BO_learning_rate.ipynb)
2) [Batch Size](https://github.com/AC-BO-Hackathon/Chihuahuas/blob/main/BO_batch_size.ipynb)
3) [Number of Neurons](https://github.com/AC-BO-Hackathon/Chihuahuas/blob/main/BO_n_neurons2.ipynb)

Results:
|   N  | Learning Rate          | Loss            |
|------|------------------|-----------------|
|  200 | 0.084878         | 0.010064        |
|  400 | 0.059692         | 0.003261        |
|  600 | 0.055656         | 0.003610        |
|  800 | 0.029240         | 0.001820        |
| 1000 | 0.017758         | 0.001970        |
| 1200 | 0.027993         | 0.003351        |
| 1400 | 0.018717         | 0.002034        |
| 1600 | 0.023550         | 0.002136        |
| 1800 | 0.014614         | 0.002025        |
| 2000 | 0.009610         | 0.001134        |

![](https://github.com/AC-BO-Hackathon/Chihuahuas/blob/main/LR.png)

|   N  | Batch Size | Loss       |
|------|--------|------------|
|  200 | 120    | 0.0080974  |
|  400 | 21     | 0.002841   |
|  600 | 27     | 0.002955   |
|  800 | 16     | 0.002613   |
| 1000 | 22     | 0.002506   |
| 1200 | 22     | 0.002462   |
| 1400 | 30     | 0.001593   |
| 1600 | 16     | 0.002007   |
| 1800 | 18     | 0.002203   |
| 2000 | 16     | 0.002041   |

![](https://github.com/AC-BO-Hackathon/Chihuahuas/blob/main/BS.png)

|   N  | # of Neurons | Loss       |
|------|--------|------------|
|  200 | 111    | 0.0084131  |
|  400 | 47     | 0.0043065  |
|  600 | 51     | 0.002910   |
|  800 | 32     | 0.002574   |
| 1000 | 22     | 0.002193   |
| 1200 | 34     | 0.002597   |
| 1400 | 22     | 0.002111   |
| 1600 | -    | -        |
| 1800 | 48     | 0.001758   |
| 2000 | 59     | 0.001668   |

![](https://github.com/AC-BO-Hackathon/Chihuahuas/blob/main/NN.png)

Conclusion

Bayesian Optimization was used to find the best hyperparameters of Graph Convolutional Neural Networks trained with subsets of small size of the QM9 Dataset, from 200 to 2000 molecules. We find that even for the lowest subset, the loss obtained for the best hyerparameters is acceptable, although clearly there is a dependence with the size of the dataset, showing better performance as N increases. However, the time consumed to reach convergence also increases rapidly, making it clear that it is worth doing this kind of fine tunning of hyperparameters. 

References:

1. Anatole von Lilienfeld and Kieron Burke. “Retrospective on a decade of machine learning for chemical discovery”. In: Nature Communications 11.1 (Sept. 2020). DOI: 10.1038/s41467- 020- 18556- 9. URL: https:
//doi.org/10.1038/s41467-020-18556-9.
