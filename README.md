# Flower-Image-Recongnition-PyTorch
Usando transfer learning e a biblioteca PyTorch para criar um classificador de espécies de flores

Neste projeto foi usado uma base de dados com 102 espécies de flores. Base esta que pode ser baixada a partir do seguinte link:
https://s3.amazonaws.com/content.udacity-data.com/courses/nd188/flower_data.zip

No arquivo trainingNN.ipynb tem todo o procedimento de download e extração da base, sendo assim não precisa fazer o download previamente.

A ideia deste projeto era usar tranferência de aprendizado com a biblioteca PyTorch, no entanto apesar de simples houve alguns impedimentos, que serão explicados como foram contornados a seguir. 

# Falta de hardware adequado para processamento
Nem sempre temos um hardware próprio para processamento de grandes bases de dados, dessa forma para contornar esse problema foi usado o Google Colab, uma ferramenta gratuita que permite que qualquer pessoa possa usufruir de processamento em GPU para construir modelos de aprendizado profundo.

O tempo de treinamento não foi contado metodicamente, no entanto durou aproxidamente 4 horas para treinar 12 épocas, com tamanho de batch igual a 64 na base de treino e 32 na base de validação.

# Dificuldade no acesso aos pesos calculados
Por razão da rede neural ter sido treinada no Google Colab, tive uma certa dificuldade para acessar os pesos do modelo ao fim do treinamento, esse problema foi contornado com o uso da biblioteca PyDrive. A biblioteca foi usada para realizar o upload do arquivo com os pesos, chamado de checkpoint.pth, para o meu Drive.
