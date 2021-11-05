# Linguagem-e-Python-POO-


1) Faça um programa que leia a idade de uma pessoa expressa em dias e
mostre-a expressa em anos, meses e dias.

data = int(input("Digite a data do seu nascimento: ")) # Data do nascimento
mes = int(input("Digite o mês do seu nascimento: ")) # Mês do nascimento
ano = int(input("Digite o ano do seu nascimento: ")) # Ano do nascimento
data2 = int(input("\nDigite a data atual: ")) # Data atual
mes2 = int(input("Digite o mês atual: ")) # Mês atual
ano2 = int(input("Digite o ano atual: ")) # Ano atual
idade_anos = ano2 - ano # Calculando a idade da pessoa
# Aqui abaixo iremos checar se o usuário já completou ano
if mes >= mes2: # Se o mês do aniversário for maior que o mês atual
    if mes == mes2: # Se o ambos os meses forem iguais
        if data > data2: # Checamos os dias
            idade_anos - 1 # Se a data de nascimento for maior que a atual, quer dizer que o usuário ainda não completou ano
                            # Por isso decrementamos 1 em idade anos, pois a idade que tinha ali era a idade que ele iria completar
    else:
        idade_anos - 1 # Se o mês for maior, o mesmo acontece.
        # A decrementação só ocorre uma vez.
dias_passados =  (30 - data) + ((12 - mes)*30) + ((mes2 - 1)*30) + data2 + (idade_anos)*365




2)Elaborar um programa que lê 3 valores a,b,c e verifica se eles formam
ou não um triângulo. Supor que os valores lidos são inteiros e positivos. Caso
os valores formem um triângulo, calcular e escrever a área deste triângulo. Se
não formam triângulo escrever os valores lidos. (Se a > b + c não formam
triângulo algum, se a é o maior).


print('###### Calculo Triângulo ######\n')
print('Digite os valores de a, B e C')
a = int(input('Valor de A: '))
b = int(input('Valor de B: '))
c = int(input('Valor de C: '))
if a > b+c:
    print('\n#############################\n')
    print(f'Valor de A: {a}\nValor de B: {b}\nValor de C: {c}\nEsses valores não formam um triângulo.')
else:
    # Calculo do perimetro:
    s = (a + b + c) / 2
    # Calculo da area
    area = (s*(s-a)*(s-b)*(s-c)) ** 0.5
    print(f'A area do triângulo é de {area:.2f}')



3) Faça um programa que leia 3 números inteiros e mostre o menor deles
primeiro = int(input('Primeiro numero: '))
    segundo  = int(input('Segundo numero : '))
    terceiro = int(input('Terceiro numero: '))

    # Achando o maior número
    maior = primeiro

    if (segundo > maior):
        maior = segundo
    if (terceiro > maior):
        maior = terceiro

    print('Maior: ',maior)

    # Achando o menor número
    menor = primeiro

    if (segundo < menor):
        menor = segundo
    if (terceiro < menor):
        menor = terceiro

    print('Menor: ',menor)


4) Implementar uma função que retorne verdadeiro se o número for primo
(falso caso contrário). Testar de 1 a 100.
	
print('######### Descobrindo Números Primos #########\n')
n = int(input('Digite um número: '))
tot = 0
for c in range(1, n + 1):
  if n % c == 0:
    print('\033[33m', end='')
    tot += 1
  else:
    print('\033[31m', end='')
  print(f'{c}', end='')
print(f'\n\033[m0 número {n} foi divisível {tot} vezes.')
if tot == 2:
  print('É um número PRIMO.')
else:
  print('Não é um número PRIMO.\n')
print('###############################################')


5) Escreva uma função que:


a) Receba uma frase como parâmetro.

frase = str(input('Digite uma frase: '))

b) Retorne uma nova frase com cada palavra com as letras invertidas.

print('##### Invertendo Frases #####\n')
frase = str(input('Digite uma frase: '))
invertida = ' '.join(palavra[::-1] for palavra in frase.split())
print(invertida)
print('\n#############################')
