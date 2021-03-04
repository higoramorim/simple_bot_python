# simple_bot_python

import os 
 
# create function to define questions
def processar_resposta(resposta, nome):
  if resposta == '1':
    print(f'{os.linesep}{nome} um triangulo tem 3 lados{os.linesep}')
  elif resposta == '2':
    print(f'{os.linesep}{nome} a soma dos angulos internos de triangulo são 180º{os.linesep}')
  elif resposta == '3':
    print(f'{os.linesep}{nome} a formula matematica de um triangulo de pitagores é: a² = b² + c², onde a é hipotenusa, ou seja o lado oposto ao ângulo de 90º com b e c como catetos que correpondem aos demais lados do triangulo{os.linesep}')
  elif resposta == '4':
    print(f'{os.linesep}{nome} a fórmula da lei dos cossenos é: a² = b² + c² - 2.b.c.cos(alfa), onde a, b e c são os lados do triangulo, cujo angulo tratado no coseno corresponde é oposto ao primeiro elemento na formula {os.linesep}')
  else:
    print('digite apenas 1, 2, 3 ou 4')
    
# create a function to build the basis of app
def start():
  # apresentar o chatbot
  print('Olá Bem vindo')
  # pedir o nome
  nome = input('digite seu nome: ')
  # pedir email
  email = input('digite seu email: ')
  # oferecer menu de opções
  
  # infinite loop to continuos answers
  while True:
      resposta = input(
        f'O que gostaria de saber hoje?{os.linesep}[1]-Quantos lados tem um triangulo?{os.linesep}[2]-Quanto vale a soma dos angulos internos de um triangulo?{os.linesep}[3]-Qual é a formula matematica de um triangulo de pitágoras?{os.linesep}[4]-Qual é a formula da lei dos cossenos?{os.linesep}')
        #processar a resposta enviada
      processar_resposta(resposta, nome)

if __name__ == "__main__":
  start()
