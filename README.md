# DeepMirror Task (ML Engineer)

### The Approach

#### Preparation - 2 hours

The preparation of the task was both theoretical and practical. On the theorectical side I learnt about the theory of graph neural networks, specifically message-passing neural networks. I also learnt how to represent molecular data (in the SMILES format) as differnt descriptors that can be inputted into machine learning model. On the practical side I learnt how to use the TDC, DeepPurpose and DeepChem python libraries. I have done this learning along with some initial idea testing (described in the next section) in the Rough.iypnb file

#### Experimentation and Documentation - 2 hours

My initial plan to approach this was to train and test all 3 models on all the ADME datasets from TDC and benchmark the models based on overall performance (a ranking). This would provide the greatest insight into the generalisability of the models to prediciting molecular properties. I did some rough testing of this in the Rough.iypnb file but realised that this approach would take too long especially as there were incompatibilities with some of the TDC datasets and DeepPurpose functions.

For time efficiency and interpretability I decided to train and test each of the models on datasets from each of the ADME properties. This would still allow a level of genernalisation to be part of the performance benchmarking. The combination of datasets chosen was made to have the greatest number of samples but also to have both regression and classification tasks. A scaffold split was chose to try and replicate the real-world where drug structures evolve over time.

For the XGBoost models, extra consideration into the feature descriptor had to be made. Popular fingerprints were considered, however I decided to go with MACCS as it was relatively low dimensional compared with the other popular fingerprints and the datasets had a relatively low number of samples. (I also experimented with PubChem fingerprints, however the descriptors took much longer to generate)

**The experimentation code and results for the sales team can be found in the Benchmaking.iypnb file**


#### Improvements

With more time, I would have liked to have done small hyperparameter tuning on each of the models and a little feature selection on XGBoost in order to evaluate the potential the optimised models have. In the experimentation no hyperparameter tuning (default parameter were used) and little feature selection was done. It was seen as "fair" because no models were optimised.

