# BSO Image Calassifications

Notebooks and models to classify images in the BSO project. Currently used for selecting the images to be passed to SmapShot

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