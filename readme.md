# OpenCV Face Recognizer
Basado en el proyecto de Adrian Rosebrock https://www.pyimagesearch.com/2018/09/24/opencv-face-recognition/
## Dependencias

- imutils
- scikit-learn
- opencv-contrib-python

`pip install imutils scikit-learn opencv-contrib-python`
## Como usar
### 1. extract_embeddings
Añade las imagenes de referencia a la carpeta dataset, usando el nombre de la persona como nombre de carpeta. P.ej dataset/{nombre}/{imagen}
```
python extract_embeddings.py --dataset dataset --embeddings output/embeddings.pickle --detector face_detection_model --embedding-model openface_nn4.small2.v1.t7
```

### 2.  train_model
  ```
  python train_model.py --embeddings output/embeddings.pickle --recognizer output/recognizer.pickle --le output/le.pickle
  ```
### 3. recognize-folder

Añadir imagenes que quieras reconocer a la carpeta images
 ```
 python .\recognize-folder.py --detector face_detection_model --embedding-model openface_nn4.small2.v1.t7 --recognizer output/recognizer.pickle --le output/le.pickle
 ```