# Cats_and_Dogs_Classification_Conv2d
Nous avons mis en place un modele de CNN (Convolution Neural Network) ou (Reseaux de neurones a convolutions), pour classifier les Chats et les Chiens.
- Lien du dataset : https://www.kaggle.com/tongpython/cat-and-dog
- dataset -> train_set
-                     -> cats 
-                     -> dogs
-            test_set
-                     -> cats 
-                     -> dogs

Nous traiterons de vrais fichiers d'images, et NON de tableaux numérisés. Ce qui signifie qu'une grande partie de ce processus consistera à apprendre à travailler et à traiter de grands groupes de fichiers d'images. Il y a trop de données pour qu'elles tiennent en mémoire sous forme de tableau numérique, nous devrons donc les introduire par lots (Batch) dans notre modèle.
# Demarche
- 1 Visualisation des images
- 2 Nombre d'images (train->4000 et test->4000)
- 3 Taille des images en moyenne : (356,409,3)
- 4 Manipulation et generation d'images : (ImageDataGenerator, flow_from_directory)
- 5 Creation de modele : Avec une architecture CNN 
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d (Conv2D)              (None, 148, 148, 32)      896       
_________________________________________________________________
max_pooling2d (MaxPooling2D) (None, 74, 74, 32)        0         
_________________________________________________________________
conv2d_1 (Conv2D)            (None, 72, 72, 64)        18496     
_________________________________________________________________
max_pooling2d_1 (MaxPooling2 (None, 36, 36, 64)        0         
_________________________________________________________________
conv2d_2 (Conv2D)            (None, 34, 34, 64)        36928     
_________________________________________________________________
max_pooling2d_2 (MaxPooling2 (None, 17, 17, 64)        0         
_________________________________________________________________
flatten (Flatten)            (None, 18496)             0         
_________________________________________________________________
dense (Dense)                (None, 128)               2367616   
_________________________________________________________________
activation (Activation)      (None, 128)               0         
_________________________________________________________________
dropout (Dropout)            (None, 128)               0         
_________________________________________________________________
dense_1 (Dense)              (None, 1)                 129       
_________________________________________________________________
activation_1 (Activation)    (None, 1)                 0         
=================================================================
Total params: 2,424,065
Trainable params: 2,424,065
Non-trainable params: 0

# Evaluation
- Loss : 0.32
- Score : 0.86
