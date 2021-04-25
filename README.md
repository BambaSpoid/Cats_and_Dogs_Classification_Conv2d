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
Total params: 2,424,065
Trainable params: 2,424,065
Non-trainable params: 0

# Evaluation
- Loss : 0.32
- Score : 0.86
