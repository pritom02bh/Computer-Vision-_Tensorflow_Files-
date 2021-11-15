## Custom Dataset for Images

* Structured In Subfolders.

      |--Dogs
      |    |-- Image1.jpg
      |    |-- Image2.jpg
      
      |--Cats
      |    |-- image1.jpg
      |    |-- image2.jpg

  #### Methods to Load these data:
  
  ``` 
      import tensorflow as tf
      from tensorflow import keras
      from tensorflow.keras import layers
      from tensorflow.keras.preprocessing.image import ImageDataGenerator
      
      img_height = 28
      img_width = 28
      batch_size = 2
      
      model = keras.Sequential([
           layers.Imput((28, 28, 1)),
           layers.Conv2D(16, 3, padding = 'same'),
           layers.Conv2D(32, 3, padding = 'same'),
           layers.MaxPooling2D(),
           layers.Flatten(),
           layers.Dense(10),
      ])
  ```
      
  #### Method One:
  
      ```
        ds_train = tf.keras.preprocessing.image_dataset_from_directory(
               'data/mnist_subfolders/',
               labels = 'inferred',
               label_mode = "int",        # Categorical, Binary
               # class_mode = ['0', '1', '2', ...]
               color_mode = 'rgb',
               image_size = (image_height, image_width),
               shuffle = True,
               validation_split = 0.1,
               subset = 'training',
               )
               
        ds_validation = tf.keras.preprocessing.image_dataset_from_directory(
               'data/mnist_subfolders/',
               labels = 'inferred',
               label_mode = "int",        # Categorical, Binary
               # class_mode = ['0', '1', '2', ...]
               color_mode = 'rgb',
               image_size = (image_height, image_width),   # Reshape if needed
               shuffle = True,
               validation_split = 0.1,
               subset = 'validation',
               )
               
              
               
               
               
               
               
               
               
               
      
