# BSO Image Classifications

Notebooks and models to classify images in the BSO project. Currently used for selecting the images to be passed to [Smapshot](https://smapshot.heig-vd.ch/).

## How to

### Download Image Data

Download source images using:

```
python downloadImages.py
```

This downloads all images speciefied in `data/images.csv` into the `images` folder. The script takes two parameters, offset and limit, to download images in batches:

```
python downloadImages.py 100 10 # Downloads 10 images starting from the 100th row in images.csv
```

### Label Images

Start a Jupyter notebook server:

```
jupyter notebook .
```

Run `notebooks/label images.ipynb` to label the images. Saving the classifications will overwrite `data/imageAnnotations.csv`.

### Train Model

The model training follows the approach described in https://towardsdatascience.com/image-classification-using-fastai-v2-on-colab-33f3ebe9b5a3. For training using a GPU (if none is available locally), [Google Colab](https://colab.research.google.com/) can be used.

### Classify Images

Load model to classify images. Follow example in `notebooks/classify images.ipynb`.

<img width="719" alt="Screenshot 2021-03-22 at 17 42 53" src="https://user-images.githubusercontent.com/1564625/112030099-32b4b600-8b3a-11eb-8921-29d37457d7ce.png">
