# Trabalho faculdade
```Python
#Exercício 1
print("Bem-vindo a Loja do Luis Fernando de Almeida Faria") 
valor_produto = float(input("Entre com o valor do produto: ")) 
quantidade_produto = int(input("Entre com a quantidade do produto: ")) 

valor_total = valor_produto * quantidade_produto #calculamos o valor total dos produtos
print(f"O valor SEM desconto: R${valor_total:.2f}") 

if (valor_total < 2500): # se o valor for menor que R$ 2500.00 não aplicamos desconto 
  valor_com_desconto = valor_total 
elif(valor_total >= 2500 and valor_total < 6000):  #se o valor for maior ou igual que R$ 2500.00 e menor que R$6000.00 aplicamos 4% de desconto 
  valor_com_desconto = valor_total * 0.96 
elif(valor_total >= 6000 and valor_total < 10000): #se o valor for maior ou igual que R$ 6000.00 e menor que R$10000.00 aplicamos 7% de desconto 
  valor_com_desconto = valor_total * 0.93 
else: 
  valor_com_desconto = valor_total * 0.89 #se o valor for maior ou igual que R$ 10000.00 aplicamos 11% de desconto 

print(f"O valor COM desconto: R${valor_com_desconto:.2f}") 


# Exercício 2
print("""Bem-vindo a Loja de Gelados do Luis Fernando de Almeida Faria
---------------------------Cardápio--------------------------
-------------------------------------------------------------
-----------| Tamanho |  Cupuaçu (CP) |  Açaí (AC) |----------
-----------|    P    |    R$  9.00   |  R$ 11.00  |----------
-----------|    M    |    R$ 14.00   |  R$ 16.00  |----------
-----------|    G    |    R$ 18.00   |  R$ 20.00  |----------
-------------------------------------------------------------""")

total = 0 #variável para receber o valor total do pedido
sabores = ["cp", "ac"] # array para guardas os sabores
tamanhos = ["p", "m", "g"] #array para guardar os tamanhos

while True:
    sabor = input("Entre com o sabor desejado (CP/AC): ").lower()
    if sabor not in sabores: #aqui comparamos se o sabor digitado pelo usuário está inserido no array de sabores
        print("Sabor inválido. Tente novamente.")
        continue

    while True:
        tamanho = input("Enter com o tamanho desejado (P/M/G): ").lower()
        if tamanho not in tamanhos: #aqui comparamos se o tamanho digitado pelo usuário está inserido no array de tamanhos
            print("Tamanho inválido. Tente novamente.")
        else:
            break
   # nesse bloco de if e elif comparamos cada umas das condições para atribuir os valores unitários de cada produto
    if sabor == 'cp' and tamanho == 'p':
        valor_unitario = 9
        print("Você pediu um Cupuaçu no tamanho P: R$ 9.00")
    elif sabor == 'cp' and tamanho == 'm':
        valor_unitario = 14
        print("Você pediu um Cupuaçu no tamanho M: R$ 14.00")
    elif sabor == 'cp' and tamanho == 'g':
        valor_unitario = 18
        print("Você pediu um Cupuaçu no tamanho G: R$ 18.00")
    elif sabor == 'ac' and tamanho == 'p':
        valor_unitario = 11
        print("Você pediu um Açaí no tamanho P: R$ 11.00")
    elif sabor == 'ac' and tamanho == 'm':
        valor_unitario = 16
        print("Você pediu um Açaí no tamanho M: R$ 16.00")
    else:
        valor_unitario = 20
        print("Você pediu um Açaí no tamanho G: R$ 20.00")

    total += valor_unitario

    continuar = input("Deseja mais alguma coisa? (S/N): ").lower()
    if continuar == 'n':
        break

print(f"O valor total a ser pago: R${total:.2f}")
```