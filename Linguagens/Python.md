# List Comprehension
Utilizando list comprehension podemos gerar novas listas com dados processados a partir de outro iterável.
Sintaxe:
```
[dado for dado in iterável]
```
Exemplos:
```
numeros [1, 2, 3, 4, 5]

res = [numero * 10 for numero in numeros]
```
```
>> [10, 20, 30, 40, 50]
```
Pode-se usar a list comprehension com condicionais, exemplo:
```
pares = [numero for numero in numeros if not numero % 2 ]
```
# Listas Aninhadas
As listas no python fazem o papel dos arrays em outras linguagens. Já as listas aninhadas fazem o papel de arrays multidimensionais. 
Exemplo de listas aninhadas:
```
listas = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```
Para acessar os elementos indexamos, por exemplo: `lista[0][1]`.
Iterando em listas aninhadas:
```
for lista in listas:
	for elemento in lista:
		print(elemento)
```
Com list comprehension:
```
[[print(valor) for valor in lista] for lista in listas]
```

# Dictionary Comprehension
```
{chave: valor for valor in iterável}
```
Exemplo:
```
numeros = {'a': ', 'b': 2, 'c': 3, 'd': 4, 'e': 5}

quadrado = {chave: valor**2 for chave, valor in numeros.items()}

numero = [1, 2, 3, 4, 5]
res = {num: ('par' if num % 2 == 0 else 'impar') for num in numero}
```
# Set Comprehension
```
numeros{num for num in range(1, 7)}
```
O mesmo vale para a tupla.
# Expressão Lambda
São funções sem nome, ou seja, funções anônimas.
Exemplo:
```
lambda x: 3 * x + 1
```
Para utilizar a expressão:
```
calc = lambda x: 3 * x + 1
print(calc(4))
```
Lambdas com múltiplas entradas:
```
nome_completo = lambda nomes, sobrenome: nome.strip().title() + ' ' + sobrenome.strip().title()
```
# Map
Faz o mapeamento de valores para uma função. Primeiro argumento é a função e o segundo é o iterável. Retorna um Map Object. 
```
def area(r):
	return 3.14 * (r ** 2)
	
raios = [2, 5, 7.1, 0.3, 10, 44]

areas = map(area, raios)
```
Após utilizar a função map, o resultado dele zerá após o primeiro uso do resultado