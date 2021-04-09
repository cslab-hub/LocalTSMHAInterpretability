# Local-Time-Series-Interpretability-over-MHA

## NOTE:
Code and information about the project is still in preparation and will soon be provided!

## Description

The given code can provide a local abstraction of time series data based on MHA. To archive this, we train a transformer model on a time series classification problem which was symbolified by the SAX algorithm. Over two given thresholds the MHA attention matrix is used to abstract the data. The code further includes a visualisation for local interpretability over the abstracted data. With a human in the loop process, a human can use the local visualisation to improve the thresholds for each dataset/classification problem. Additionaly a re-evaluation model is trained to show how well the reduced data performes and by how much the data is reduced. We argue that the visualized abstractions are better interpretable than the normal inputdata, which is helpful to understand the underlying classification problem.


The project contains a jupyter notebook which provides the model from the publication and also includes the weights for the published results (in the zip "saves_paper"). The code uses by default two datasets (linked below) and trains 5 folds for cross-validation. Each fold trains 5 models: 
- Normal input data
- Symbolic data (SAX)
- Average based threshold with interpolated missing data
- Average based threshold with mising data masked
- Max based theshold with interpolated missing data
- Max based threshold with mising data masked

At the end of the notebook the abstracted data can be analysed with the given visualisations.

## Dependencies
A list of all needed dependencies:



## Cite and publications
This code represents the used model for the following publication: TODO

Preprint: https://martin.atzmueller.net/paper/VisualizingAbstractedTransformerAttentionLocalInterpretability-SchwenkeAtzmueller-2021-preprint.pdf

If you use, build upon this work or if it helped in any other way, please cite the linked publication.


## Datasets

Included datasets are:

http://www.timeseriesclassification.com/description.php?Dataset=SyntheticControl
http://www.timeseriesclassification.com/description.php?Dataset=ECG5000
