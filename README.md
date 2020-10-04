### Objective

To develop a cloud effective radius (CER) and optical thickness (COT) retrieval framework using python; scikit-learn and TensorFlow: An example of application with the Moderate Resolution Imaging Spectroradiometer (MODIS) on board NASA's Terra & Aqua satellites.

### Updates

10-04-2020: update python code to download the ice and liquid reflectance libraries

09-15-2020: start the project

### Download the project

git clone https://github.com/benjamin-hg-marchant/deep-inversion.git

Read the [doc](https://github.com/benjamin-hg-marchant/deep-inversion/blob/master/docs/train_deep_learning_model_from_modis_myd06_lut.ipynb)

### Download the reflectance libraries with python

    url = 'https://atmosphere-imager.gsfc.nasa.gov/sites/default/files/ModAtmo/resources/modis_c6_luts.tar.gz'
    
    downloaded_filename = 'modis_c6_luts.tar.gz'
    
    urllib.request.urlretrieve(url, downloaded_filename)
    
    # Unzip .tar.gz
    # Ref: https://stackoverflow.com/questions/30887979/i-want-to-create-a-script-for-unzip-tar-gz-file-via-python
 
    fname = 'modis_c6_luts.tar.gz'

    if fname.endswith("tar.gz"):
   
        tar = tarfile.open(fname, "r:gz")
        tar.extractall()
        tar.close()
