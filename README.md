							
PREPARAR LA CHATBOT DATABASE

CREAR TRAIN.FROM Y TRAIN.TO
													




													CREAR ENVIROMENT
conda create -n Chatbot python=3.6 																		#Crearlo(una vez)


conda activate Chatbot 																				#Activarlo
conda deactivate 																				#Para Desactivarlo

												PREPARAR ENVIROMENT														

cd F:\nmt-chatbot-master

conda install git

git clone --recursive https://github.com/daniel-kukiela/nmt-chatbot

cd nmt-chatbot																			

pip install -r requirements.txt 	

cd setup																	
 						

python prepare_data.py

cd ../


												ENTRENAR

python train.py
																						
												TENSORBOARD
tensorboard --logdir=train_log/

												INTERACTUAR


python inference.py

														

												LINKS

https://pythonprogramming.net/interacting-chatbot-deep-learning-python-tensorflow/?completed=/bidirectional-attention-mechanism-chatbot-deep-learning-python-tensorflow/
https://github.com/daniel-kukiela/nmt-chatbot
https://github.com/daniel-kukiela/nmt-chatbot/blob/master/README.md


										SIGNIFICADOS


step: El número de pasos de entrenamiento completados.
lr: La tasa de aprendizaje (learning rate) utilizada en este paso.
step-time: El tiempo que toma completar un paso de entrenamiento.
wps: Palabras por segundo procesadas.
ppl (perplexity): Una medida de cuán bien el modelo predice una muestra. Valores más bajos son mejores.
gN (gradient norm): La norma del gradiente. Valores muy altos pueden indicar que el modelo está experimentando gradientes explosivos.
bleu: La puntuación BLEU, que mide la precisión de la traducción. Una puntuación de 0.00 significa que las traducciones generadas por el modelo no coinciden bien con las referencias.
