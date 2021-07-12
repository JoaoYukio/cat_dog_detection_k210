# cat_dog_detection_k210
Um detector de gatos e cachorros usando a placa MaixBit, usando o google colab e um dataset do kaggle para gerar uma "caixa" no rosto de gatos e cachorros. Esse projeto foi baseado nesse [exemplo](https://www.hackster.io/dmitrywat/object-detection-with-sipeed-maix-boards-kendryte-k210-421d55) da biblioteca aXelerate.

# Descrição
Esse projeto consiste em usar um [dataset](https://www.kaggle.com/andrewmvd/dog-and-cat-detection) que contêm fotos de gatos e cachorros e suas respectivas "caixas" no rosto dos animais( nesse caso são dois arquivos, um xml e uma imagem). 
Esse projeto é semelhante ao meu projeto de classificação de animais, e usa basicamente as mesmas ferramentas de software e hardware que essa.

Usando a plataforma aXeleRate podemos não só treinar o modelo, como podemos também visualizar os dados.

        %matplotlib inline

        from axelerate.networks.common_utils.augment import visualize_detection_dataset

        visualize_detection_dataset(img_folder='/content/drive/MyDrive/cat_dog_dataset/val/img_val', ann_folder='/content/drive/MyDrive/cat_dog_dataset/val/ann_val', num_imgs=10, img_size=224, augment=True)

![image](https://user-images.githubusercontent.com/74123993/125210467-609f4100-e276-11eb-8a4b-0bdd9a462451.png)
![image](https://user-images.githubusercontent.com/74123993/125210472-685ee580-e276-11eb-8243-087e2da45a44.png)

![image](https://user-images.githubusercontent.com/74123993/125210481-73197a80-e276-11eb-98be-7794a7a32344.png)
![image](https://user-images.githubusercontent.com/74123993/125210495-8e848580-e276-11eb-96e1-a64679d11b92.png)

O processo de treinamento pode levar algum tempo, então no [Colab](https://colab.research.google.com/drive/1HcuwZeGmcBSnQXtGyYeoRJ-W6fZodWKa?usp=sharing) coloquei dois arquivos "config", um para o treinamento do "zero" e outro com um modelo que já estava sendo treinado, já que quando começamos treinar o treinamento vai sendo salvo cada vez que um modelo consegue uma performance melhor.





