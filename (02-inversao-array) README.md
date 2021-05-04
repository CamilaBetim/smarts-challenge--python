# Desafio

Faça um script/sistema, em qualquer linguagem de programação, que faça a inversão do um array alfanumérico abaixo (não é permitido utilizar funções prontas da linguagem/framework/biblioteca):

`['The', 'quick', 'brown', 'fox', 'jumps', 'over', 'the', 'lazy', 'dog']`

# Documentação

Atualize este README sobre como rodar em desenvolvimento e como efetuar o deploy, se aplicável.

# Explicando o código:

### Primeiramente, vamos criar nossa variável array e definir os alfanúmericos que inseriremos nela:
```python
array= ["The", "quick", "Brown", "fox", "jumps", "over", "the", "lazy", "dog"]
```
### Nesta parte, iremos trazer na tela o array que armazenamos dentro da variável:
```python
print("Dados contidos no array:", array)
```
### Agora, iremos inverter nossa array:
```python
n= 0                   #aqui estamos definindo a primeira posição que é o zero, e guardando ela dentro de n 
q= len(array) - 1      #o len irá retornar quantas posições tem dentro do array, precisamos colocar o -1 pois o computador trabalha com o acesso de posição começando do 0
```
### Faremos um enquanto:
```python
while n < q:                                    #enquanto n for menor q ele fará o seguinte processo: 
                                                #1: o array[n] irá receber o array[q], e o array[q] irá receber o array[n], realizando assim a inversão
    array[n], array[q] = array[q], array[n] 
    n += 1                                      #2 aqui ele incrementa o i
    q -= 1                                      #3 aqui ele decrementa o j 
```
### Depois de finalizar o enquanto, traremos na tela o array inverso
```python
print("Array inverso:", array)

quit()
```
# Segue abaixo fotos do código feito e o resultado que trouxe. 

![image](https://user-images.githubusercontent.com/83428347/116748964-9c946b00-a9d6-11eb-9fa4-7874a037ff5f.png)
![image](https://user-images.githubusercontent.com/83428347/116749191-f301a980-a9d6-11eb-9402-e5df32d4d815.png)

# Aplicação
Podemos aplicar esse tipo de código, quando quisermos colocar em ordem uma grande quantidade de dados, ou até mesmo se temos muitos dados, verificar de forma fácil qual foi o último dado armazenado, entre outros. 
