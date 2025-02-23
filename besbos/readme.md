# How to use the scripts

You can create the datasets by your own. Extract bonescans and besilesomab scans from your PACS. 
Mininum samples should be 100 per class. All training was done on Google Colab with combination of Google Drive. We suggest to zip the dataset for
one file upload. Code is provided how to unzip it.

## Binary classification
- export any bonescan and besilesomab scan from your **PACS**
- create a folder (for example besbosbin) -> you will then need to write in the config section it in the notebook
- put them into two subfolders named **bes** and **bos**
- pictures should be cropped, removed of any metadata, size of 900(h)x252(w)
- should be in grey scale, but in RGB mode (more in the article)

## Multiclass classification
- export any bonescan and besilesomab scan from your PACS
- divide them into **four classess** *besnegat, besposit, bosnegat, bosposit*
- you can use reports, clinical feedback as a Ground thruth paramater or just the "look" analysis -> positive and negative
 - this will then make the outcome
- try to really pickup good samples, one rule if you are not sure the network will be either so really good representatives samples
- create a folder (for example besbospositnegat)
- create subfolders *besnegat, besposit, bosnegat, bosposit* and put your divided samples into them
- try to keep the balance in the classes, if not there are some examples how to augment the samples, in the article

## Traning
- you can use Google Colab -> free you will get some free time but it will not last for ever
- you can try by Colab pro -> the price is not so high
- or you can run the training locally -> you need a nvidia/CUDA for that

## Local analysis
- Jupyter Notebook was used under WSL2 (Windows Linux Subsytem)
- You can also run Jupyter notebook in native Windows
- Install Python 3.x (x>9) and Tensoroflow -> this depends on Colab but Tensorflow 2.18 is the latest
- Issue is Tensorflow uses .keras file type -> the version must be same as on Colab then locally
- You can still save in h5 format
 - load the model from Colab Cloud
 - model.summary()
 - model.save("path_to_save/model_name.h5) -> is less version dependent
- You can rewrite the local script to online scripts -> should not be complicated




