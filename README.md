# Desafio

Faça um script/sistema, em qualquer linguagem de programação, que escreva todos os número de -71 até 103. Para os números múltiplos de 3, escreva "Smart", para os números múltiplos de 5, escreva "Staff".

# Documentação

Atualize este README sobre como rodar em desenvolvimento e como efetuar o deploy, se aplicável.

#Início do Script

valor= -71                             #definimos aqui o valor inicial que iremos mostrar

while valor <= 103:                    #fazemos um enquanto, para que o programa faça esse processo abaixo até que ele seja menor ou igual a 103.  
    if valor%3 == 0:                   #se a divisão por 3 da varíavel valor for igual a 0, então ele trará na tela a palavra "Smart"       
       print ("Smart")
    else:
         if valor%5 == 0:              #se a divisão por 5 da varíavel valor for igual a 0, então ele trará na tela a palavra "Staff"
            print ("Staff")
         else:
             print (valor)             #se a divisão da variável valor por 5 ou 3 não der 0, ele trará na tela o número armazenado dentro dessa variável.
    valor=valor+1                      #precisamos no final, armazenar na varíavel valor a soma valor+1, para que ele possa trazer o número posterior ao armazenado antes

quit()

#Fim do Script

![image](https://user-images.githubusercontent.com/83428347/116622370-f59ec900-a91a-11eb-92ce-2ceb019539a0.png)
![image](https://user-images.githubusercontent.com/83428347/116622472-21ba4a00-a91b-11eb-9e10-d5dacd686e9f.png)
![image](https://user-images.githubusercontent.com/83428347/116622502-2c74df00-a91b-11eb-8f78-38a5b5cfa494.png)


