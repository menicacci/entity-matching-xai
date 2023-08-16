  # Counterfactual Explanations for Entity Resolution
  
  [Ditto](https://github.com/megagonlabs/ditto) represents a solution based on pre-trained language models for the Entity Resolution problem. Analyzing this model, it was observed that some of Ditto's predictions are incorrect, and it is inexplicable why the model made a certain choice. In an attempt to address this issue, techniques based on Explainable AI methods were considered.
  
  [CERTA](https://github.com/tteofili/certa) provides explanations for predictions of ER systems using methods based on saliency. Using this model, we adopted data augmentation techniques to enhance the accuracy of Ditto's predictions using counterfactual explanations (CE). A counterfactual explanation provides input samples, in our case pairs of tuples, that change a prediction into a desired outcome. 
  
  The general idea was to train the Ditto model on a specific training set and measure its performance on the corresponding test set. At that point, pairs of records in the training set that were misclassified were identified. For these pairs, CERTA was used to generate a set of counterfactual explanations. The samples obtained from these explanations were added to the original training set, and Ditto was retrained on the augmented training set. Once the training was completed, Ditto's performance on the same test set was measured once again.
  
  ![CE_for_ER_1](https://github.com/menicacci/CE_for_ER/assets/105044910/6dfd8a05-e8fd-463b-9012-624742ff41f6)
