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
      
  #### Method One:
      
