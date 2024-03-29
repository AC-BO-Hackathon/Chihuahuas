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




References:

1. Anatole von Lilienfeld and Kieron Burke. “Retrospective on a decade of machine learning for chemical discovery”. In: Nature Communications 11.1 (Sept. 2020). DOI: 10.1038/s41467- 020- 18556- 9. URL: https:
//doi.org/10.1038/s41467-020-18556-9.
