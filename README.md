# TabNet
> A TabNet Implementation with Self Supervision


## Install environment 

`pip install -r requirements.txt`

## How to run the experiments

To rerun the experiments, you can run the `experiment.ipynb` notebook. If you want a different dataset, replace the `load_x` function with the one you want from `utils.py`. The `load` functions take care of downloading the data.

## Code Structure

The code was written solely in notebooks and "exported" to `.py` files using the awesome [nbdev](https://nbdev.fast.ai/) project. 

The final .py files can be found in the `tabnet` directory, howevery you can see the original implementation and tests in the equivalently named notebook. 

The final files: 
1. core.py - implementations of `Sparsemax`, and `Ghost Batch Normalization`
1. model.py - Includes all the relevant model classes (encoder, decoders, classifier heads, loss functions, relevant callbacks etc)
1. utils.py - Helper functions that help:
    * load / download the data & model params 
    * model builders (putting together encoder, decoder from the models.py module)
    * experiment helps - such as `score_before_after_ss` which run the model before and after self supervision and return the final accuracy.
