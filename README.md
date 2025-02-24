# The Cat's Meow
**An Unsupervised Learning Approach to classifying cat sounds**

I'm convinced my cat thinks I'm a complete ignoramus because I haven't learned a lick of "cat" in our 10 years together. It's not a difficult language. The grammar is straightforward; the vocabulary is limited. Let's see if we can use Unsupervised Machine Learning to help learn more about the types of things cats say. 

![cat-shouting-through-megaphone-blue-backgroundgenerative-ai](https://static.wixstatic.com/media/080994_44699c84709444fdad664c1d431384d0~mv2.jpg/v1/fill/w_815,h_635,al_c,q_85,usm_0.66_1.00_0.01,enc_avif,quality_auto/cat-shouting-through-megaphone-blue-backgroundgenerative-ai%20(1).jpg)

This notebook uses the [Cat Meow Classification](https://www.kaggle.com/datasets/andrewmvd/cat-meow-classification) dataset on Kaggle, which includes 440 audio recordings of cat meows in three contexts: brushing, waiting for food, and isolation in an unfamiliar environment. These contexts can help us evaluate the performance of unsupervised algorithms in grouping recordings based on context.

## Environment
To reproduce this workflow, use the provided environment.yml file to create a conda environment (you should already have Python and conda installed on your system).

After cloning this directory to your system, use the following bash commands to create and activate the environment:

```bash
conda env create -f environment.yml
conda activate meow
```
You must have Jupyter Notebook installed on your system to run this analysis. For installation instructions, consult the documentation [here](https://jupyter.org/).

> [!Warning]
> As of Python 3.13, packages `aifc` and `sunau`, both dependencies of `librosa` were removed from the core Python library. Use 
> ```
> pip install standard-aifc
> pip install standard-sunau
> ```
> until `librosa` is updated. (This should occur automatically if using the `environment.yml` file).

## Data
This notebook loads the cat-meow-classification dataset directly from Kaggle. You must download a Kaggle API token (find instructions [here](https://www.kaggle.com/docs/api#authentication)).

## Workflow
Run the meow.ipynb notebook in your preferred environment.