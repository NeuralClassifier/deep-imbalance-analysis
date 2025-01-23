# The class imbalance problem in deep learning

***Published the Machine Learning Journal***

**Paper URL:** [Springer Nature](https://link.springer.com/article/10.1007/s10994-022-06268-8)

**Abstract:** Deep learning has recently unleashed the ability for Machine learning (ML) to make unparalleled strides. It did so by confronting and successfully addressing, at least to a certain extent, the knowledge bottleneck that paralyzed ML and artificial intelligence for decades. The community is currently basking in deep learning’s success, but a question that comes to mind is: have all of the issues previously affecting machine learning systems been solved by deep learning or do some issues remain for which deep learning is not a bulletproof solution? This question in the context of the class imbalance becomes a motivation for this paper. Imbalance problem was first recognized almost three decades ago and has remained a critical challenge at least for traditional learning approaches. Our goal is to investigate whether the tight dependency between class imbalances, concept complexities, dataset size and classifier performance, known to exist in traditional learning systems, is alleviated in any way in deep learning approaches and to what extent, if any, network depth and regularization can help. To answer these questions we conduct a survey of the recent literature focused on deep learning and the class imbalance problem as well as a series of controlled experiments on both artificial and real-world domains. This allows us to formulate lessons learned about the impact of class imbalance on deep learning models, as well as pose open challenges that should be tackled by researchers in this field.


This code correspondes to the paper entitled 'The Class Imbalance Problem in Deep Learning' published in the Special Issue on Imbalanced Learning in the journal Machine Learning with co-authorship from:

Roberto Corizzo - rcorizzo@american.edu Nathalie Japkowicz - japkowic@american.edu Kushankur Ghosh - kushanku@ualberta.ca Paula Branco - pbranco@uottawa.ca Bartosz Krawczyk - bkrawczyk@vcu.edu

The objective of the paper is to asses the affectiveness of depth at mitigating bias due to class imbalance, and to how this is impacted by problem complexity.

EXPERIMENTS
-------------------------------------------
-------------------------------------------
Data
-------------------------------------------

Backbone datasets: synthetic tabular dataset that corresponds to the imbalance analysis originally undertaken in  in Japkowicz and Stephen (2002)

Image datasets: imbalanced versions of CIFAR-10 and MNIST-Fashion, plus imbalanced versions of Shapes dataset proposed by (El Korchi and Ghanou in 2020)

Text datasets: imbalanced versions of 20NewsGroup (Alhenaki and Hosny, 2019) and Job Classification (https://www.kaggle.com/adarshsng/predicting-job-type-category-by-job-description?select=train.csv)

The datasets are not included in this repository due to storage limitations but are available upon request

Deep networks
-------------------------------------------
MLP: Deep versions of the MLP (fully connected deep network) were applied to the backbone and text datasets. The text datasets were pre-processed with TF-IDF prior to input in the network. 

CNN: Standard CNN architectures were used for the text data

The code for the deep learning models is contained in src/models/ backbone_mlp.py, text_mlp.py, mnistFahsion_cifar10_cnn.py, and shapes_cnn.py

Execution
-------------------------------------------

The sweep of experiments for each datasts across imbalance levels and model depths can be executed with the python run scripts: run[DATASET_NAME].py. The runner saves pickle files in the corresponding results directory. The pickle files contain lists of the sweep of runs. Finally, the compleRults.py code can be used to reformate the saved pickle results files into CSV files. 

Results
-------------------------------------------
Performance is assessed based on the average g-mean


## Citation: 
```
@article{ghosh2024class,
  title={The class imbalance problem in deep learning},
  author={Ghosh, Kushankur and Bellinger, Colin and Corizzo, Roberto and Branco, Paula and Krawczyk, Bartosz and Japkowicz, Nathalie},
  journal={Machine Learning},
  volume={113},
  number={7},
  pages={4845--4901},
  year={2024},
  publisher={Springer}
}
```
