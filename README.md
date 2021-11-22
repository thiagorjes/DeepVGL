# DeepVGL

DeepVGL (Deep Visual Global Localization) é um sistema de localização global baseado em redes neurais profundas que usa imagens
para localização global de robôs em mapas de grid.


baixe o dataset de validação para fins de avaliar a acurácia do DeepVGL em pytorch
 
https://drive.google.com/file/d/1HdcwCLmz833dgZzPHDbUZtzLM_SMvO3S/view?usp=sharing

Descompact o valid.tgz e mova a pasta "dados" para "/dados/"

Crie o arquivo valid.list com o seguinte comando:

```bash

cd /dados/ufes
echo "generating darknet image list for valid"
ls `pwd`/valid/*.png > /dados/ufes/ordered.list
shuf /dados/ufes/ordered.list > /dados/ufes/valid.list

```

Caso possua o dataset de treino, execute o seguinte comando para criar o arquivo train.list

```bash

cd /dados/ufes
echo "generating darknet image list for train"
ls `pwd`/train/*.png > /dados/ufes/ordered.list
shuf /dados/ufes/ordered.list > /dados/ufes/train.list

```

Se não possuir o dataset de treino e quiser apenas testar a acurácia execute o seguinte comando para gerar o arquivo train.list vazio


```bash

cd /dados/ufes
echo "generating darknet image list for train"
echo "" > /dados/ufes/train.list

```

@misc{lightnet18,
  author = {Tanguy Ophoff},
  title = {Lightnet: Building Blocks to Recreate Darknet Networks in Pytorch},
  howpublished = {\url{https://gitlab.com/EAVISE/lightnet}},
  year = {2018}
}
