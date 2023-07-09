# Desafio

Dado o array de entrada abaixo:

`['ab', 'bc', 'abc', 'cba', 'ab', 'ab', 'cba']`

E dado o array de verificação abaixo:

`['ab', 'cba', 'bb']`

Faça um script/sistema, em qualquer linguagem de programação, que conte, e retorne um array com o resultado, de quantas vezes cada elemento do array de `verificação` existe no array de `entrada` (não é permitido utilizar funções prontas da linguagem/framework/biblioteca).

O resultado deve ser um array como o abaixo:

`[3, 2, 0]`

# Documentação

Atualize este README sobre como rodar em desenvolvimento e como efetuar o deploy, se aplicável.

# Como desenvolver o script 

### Primeiro nós criamos as variáveis que vão aramazenar nossos arrays, uma para o array de entrada e outra para o array de verificação:
```python
entrada= ["ab", "bc", "abc", "cba", "ab", "ab", "cba"]
verificacao= ["ab", "cba", "bb"]
```
### Após isso iremos trazer na tela quais são os valores do array de entrada e do array de verificação:
```python
print("Array de entrada:", entrada)
print()
print("Array de verificação:", verificacao)
print()
```
### Agora iremos criar algumas variavéis que irão nos ajudar no processo:
```python
contador=0          #Irá armazenar a quantidade de vezes que o item "ab" aparece no array de entrada
contador1=0         #Irá armazenar a quantidade de vezes que o item "cba" aparece no array de entrada
contador2=0         #Irá armazenar a quantidade de vezes que o item "bb" aparece no array de entrada
n= 0                # Essa variável irá armanezar a posição de cada valor do array 
q= len(entrada)     # Essa variável significa a quantidade de valores que tem no array entrada
```

### Iremos fazer um enquanto, que irá verificar se os valores que estão presentes array de entrada, são iguais aos valores do array de verificação:
```python
while n < q:                                         # Enquanto n for menor que a quantidade de valores que existe dentro do array entrada, fazemos:
    if entrada[n] ==verificacao[0]:                 # Se o valor que está na posição 0 do array de entrada, for igual ao valor que está na posição 0 do array de verificação
       contador=contador+1                          # O contador irá adicionar 1 
    else:
         if entrada[n] ==verificacao[1]:            # Se o valor que está na posição 0 do array de entrada, for igual ao valor que está na posição 1 do array de verificação
            contador1=contador1+1                   # O contador1 irá adicionar 1
         else:
              if entrada[n] ==verificacao[2]:       # Se o valor que está na posição 0 do array de entrada, for igual ao valor que está na posição 2 do array de verificação
                  contador2=contador2+1             # O contador2 irá adicionar 1 
    n=n+1                                           # Depois disso ele adicionará mais 1 na variável n, para fazer o mesmo processo com todos os valores do array de entrada.
 ```               
    
### Depois que ele finalizar o processo, iremos fazer um novo array com o valor contido no contador, contador1 e contador2
```python
arrayfinal= [contador, contador1, contador2]
 ```  
### E então ele trará na tela o resultado que armazenamos em cada variável dentro de um array:
```python
print("Resultado array:", arrayfinal)
 ```  
 
 # Fotos do código realizado e o resultado que obtivemos após rodá-lo:
 ![image](https://user-images.githubusercontent.com/83428347/117064374-7fc0a600-acfc-11eb-9571-44176157a0b9.png)
 
 ![image](https://user-images.githubusercontent.com/83428347/117064407-8bac6800-acfc-11eb-920b-653ee2706737.png)
 
 # Aplicação
 Podemos utilizar esse tipo de código, para encontrar determinadas palavras ou carateres em um pdf, um arquivo de texto com muita informação, basicamente uma busca para verificarmos quantas vezes aparece determinado caracter e saber se ele existe.


 
