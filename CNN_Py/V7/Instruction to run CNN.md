## How to run CNN from Google Colaboratory

1. Recieve invitation to the project from **ed2801@columbia.edu**. 
2. Pull this repository to local machine.
3. Activate Google Colaboratory and open main_new.ipynb file from there.
4. Upload contents of **lib** folder into **Files** in Google Colaboratory
5. Download training and testing image folders to Google Drive. You would need only HR images for training as corresponding LR images will be generated by the program.
6. Mount Google Drive into Google Colaboratory.
7. Update paths to your folders in the following places: 
* Step 0: path to training data
* Step 5: path to test data (in case it is different)
* inside the **train_function.py** for *generator.save()* and *generator.save_weights()*
8. Run line by line, except for 

```
#Predict snippets based on model download
image_shape - (16,16,3)
generator = model_CNN.Generator(image_shape).generator()

generator.load_weights('model.h5')

```
Use these two lines to download pre-trained model from your directory.

Note: unless you have access to higher RAM, sample maximum 450 images for training, this is maximum capacity for a training set.
