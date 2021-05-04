# Desafio

Faça um script/sistema, em qualquer linguagem de programação, que verifique quantas `voltas` existem dentro dos arrays de exemplo abaixo, levando em consideração que:
 - Cada `volta` deve ser considerada quando a mesma posição do array for visitada mais de 1 vez, na mesma `volta`
 - O número dentro do array apresentado é o índice que deve ser visitado na próxima iteração
 - O array começa no índice 0
 - Retornar o total de `voltas` dentro do array de exemplo

Exemplo 1:

`[1,2]`

A iteração começa no primeiro elemento, no índice `0`. Nesta posição está o número `1`, então a próxima iteração deverá ser no índice `1`. No índice `1` existe o valor `2`, então a próxima iteração deverá ser no índice `2`. O índice `2` não existe, então a iteração deve cessar, e nenhuma `volta` foi encontrada.

Exemplo 2:

`[1,3,4,0,2]`

Existem 2 `voltas` neste array:

`0 -> 1 -> 3 -> 0 -> fim`, 1ª `volta` encontrada
`2 -> 4 -> 2 -> fim`, 2ª volta encontrada

Arrays de entrada:

 - `[1,2,3,4,5,6,7,8,9,0]`
 - `[3,2,0,1,4]`
 - `[7,0,4,2,3,1,6]`

# Documentação

Atualize este README sobre como rodar em desenvolvimento e como efetuar o deploy, se aplicável.

# Como desevolver este Script:

### Primeiro iremos criar variáveis para armazenar nossos arrays, e vamos criar outras arrays que sevirão para armazenar a quantidade de vezes que a posição da array é visitada, significando que quando ela for visitado duas vezes na mesma volta, terá ocorrido uma volta.              
```python
array1= [1, 2, 3, 4, 5, 6, 7, 8, 9, 0]
item1= [0, 0, 0, 0, 0, 0, 0, 0, 0, 0]                          # Irá armazenar quantidade de vezes que as posições do array1 são visitadas
array2= [3, 2, 0, 1, 4]
item2= [0, 0, 0, 0, 0]                                         # Irá armazenar quantidade de vezes que as posições do array2 são visitadas
array3= [7, 0, 4, 2, 3, 1, 6]
item3= [0, 0, 0, 0, 0, 0, 0]                                   # Irá armazenar quantidade de vezes que as posições do array3 são visitadas
```
### Após isso, ele tratá na tela quais são os valores armazenados em cada array:
```python
print(" O array 1 é :", array1)
print()
print(" O array 2 é :", array2)
print()
print(" O array 1 3 :", array3)
print()
```

### Então vamos definir algumas variáveis que são de extrema importância para nosso Script:
```python
n= 0                       # A variável n vai representar as posições do array1
m= 0                       # A variável n vai representar as posições do array1
k=0                        # A variável n vai representar as posições do array1
q= len(array1)             # Representa a quantidade de posições que tem no array1
q1= len(array2)            # Representa a quantidade de posições que tem no array2
q2= len(array3)            # Representa a quantidade de posições que tem no array3
i= len(item1)              # Representa a quantidade de posições que tem no item1
i2= len(item2)             # Representa a quantidade de posições que tem no item2
i3= len(item3)             # Representa a quantidade de posições que tem no item3
contador=0                 # Irá armazenar a quantidade de voltas que possui no array1
contador1=0                # Irá armazenar a quantidade de voltas que possui no array2
contador2=0                # Irá armazenar a quantidade de voltas que possui no array3
```
### Agora iremos realizar o processo de verificação da quantidade de voltas que temos em nossos arrays:
```python
while n < q:                            # Enquanto n for menor que a quantidade de posições existentes no array1
    if 1==1:                            # Aqui nós colocamos uma condição que será sempre verdadeira ( se 1 for igual a 1 ), para ele seguir com o processo.
      item1[n] = item1[n]+1             # Nesse momento n vale 0, então ele diz: O valor presente na posição de número 0 do item1 (o array que possui todos os valores com 0)
                                        vai acrescentar +1.
      if item1[n] ==2:                  # Se  O valor presente na posição de número 0 do item1 for igual a 2, n vai receber +12.
            n = q+1
      else:
       n = array1[n]                    #Senão, n vai receber o valor da posição de número 0 do array1, e ele fará esse processo, passando por todas as posiçãoes, até n ser > q.
``` 

É importante entender a finalidade do código nessa parte: basicamente ele irá somar 1 nas posições do array item1, nesse array item1 todos os valores são 0, esses valores significam a quantidade de vezes que visitamos uma posição, por isso incialmente ele é 0. 

Então nós começamos o código visitando a posição 0 do item1, nesse momento iremos somar 1 a está posição, para entendermos que ela já foi 1 vez visitada. 

Esse valor irá passar por outra condição agora, basicamente, se o valor presente na posição 0 for 2, sabemos que ela já foi visitada duas vezes ( o que sabemos que é impossível agora pois estamos rodando a primeira posição, mas é apenas explicação). Se ela for visitada duas vezes nesse enquanto que criamos, então foi realizada uma volta, e ai o n=passará a valer q+1, então nesse caso n será maior que q, e nosso enquanto irá parar ali, não irá mais rodar.

Se a posição 0 não for = 2, então o nosso n irá receber a posição 0 do array como valor, e ele continuará o looping, passando pelas próximas posições até n ser maior que q.

### Nesse processo, veremos quais posições do array ainda não foram visitadas:
```python
for n in range(i):      # Iremos fazer um for, o n irá percorrer a quantidade de vezes que possui na variável i, essa por sua vez armazena a quantidade de posições que no item1
    if item1[n]==0:             # Aqui nós iremos fazer uma condição que, se a posição atual do item1 for igual 0, ele realizará o seguinte processo:
      while item1[n] != 2:          #1: Fará um enquanto a posição atual do item1 for diferente de 2:
           item1[n] = item1[n]+1    # A o valor existente na posição atual do item1 receberá +1
           n = array1[n]            # n irá receber o valor da posição atual do array1
           
É importante entender a finalidade do código nessa parte: Basicamente, ele irá pegar todos os valores presente no array item1, e verificar se tem algum que vale 0. Se tiver algum, significa que ele não foi visitado nenhuma vez, a volta acabou antes de chegar nele, porém precisamos rodar ele também. 
Então fazemos o seguinte proesso, iremos criar um equanto, que diz que enquanto esse valor for diferente de 2 ( ou seja enquanto não finalizar a volta), o a posição do item1 atual irá receber +1 e o logo em seguida o n irá receber o valor da posição atual do array1, e esse processo será feito em looping até item1[n] ==2.

```
### Aqui nós iremos armazenar na váriavel contador, a quantidade de vezes que o valor 2 aparece no array item1 ( ou seja, a quantidade de vezes que tivemos voltas no array)
```python
for n in range(i):                           # O n irá percorrer a quantidade de vezes que possui na variável i, essa por sua vez armazena a quantidade de posições que no item1
    if item1[n]== 2:                         # Se a posição atual do item1 for igual a 2, então o contador irá receber +1.
        contador=contador+1

É importanto observar nessa parte, que o valor contido na variável contador, é quantidade de voltar que tivemos no array1.
```

### Aqui, ele irá trazer para nós a quantidae de voltas no array1:
```python
        
print( "O número de voltas que temos no array 1, é igual a:", contador)
()
```

### Nessa parte, ele fará extamente o mesmo processo explicado acima, porém com outras váriavéis, que serão usadadas para descobrir as voltas do array2:
```python
while m < q1:
      if 1==1:
         item2[m] = item2[m]+1
         if item2[m] ==2:
            m = q1+1
         else:
          m = array2[m]
          
for m in range(i2):
    if item2[m]== 0:
      while item2[m] != 2:
           item2[m] = item2[m]+1
           m = array2[m]

for m in range(i2):
              if item2[m]== 2:
                      contador1=contador1+1
 ```                    
                      
 ### Aqui, ele irá trazer para nós a quantidae de voltas no array2:      
 ```python
print( "O número de voltas que temos no array 2, é igual a:", contador1)
()
```

### Nessa parte, ele fará extamente o mesmo processo explicado acima, porém com outras váriavéis, que serão usadadas para descobrir as voltas do array3:
```python
while k < q2:
      if 1==1:
         item3[k] = item3[k]+1
         if item3[k] ==2:
            k = q2+1
         else:
          k = array3[k]
      if k ==7:
         k = array3[1]

for k in range(i3):
    if item3[k]== 0:
      while item3[k]!= 2:
            item3[k] = item3[k]+1
            k = array3[k]


for k in range(i3):
              if item3[k]== 2:
                      contador2=contador2+1
 ```
                 
 ### Aqui, ele irá trazer para nós a quantidae de voltas no array3:     
 ```python
print( "O número de voltas que temos no array 3, é igual a:", contador2)
```
