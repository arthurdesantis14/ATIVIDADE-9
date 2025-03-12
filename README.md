# ATIVIDADE 9
## Pasta: minhasoperacoes/

# minhasoperacoes/__init__.py
__all__ = ["operacoes", "utils"]

# minhasoperacoes/operacoes.py
def soma(a, b):
    return a + b

def subtracao(a, b):
    return a - b

def multiplicacao(a, b):
    return a * b

def divisao(a, b):
    if b == 0:
        return "Erro: divisão por zero."
    return a / b

# minhasoperacoes/utils.py
def exibir_resultado(operacao, resultado):
    print(f"Resultado da {operacao}: {resultado}")

## Arquivo principal: main.py
from minhasoperacoes import operacoes, utils

op = input("Escolha uma operação (+, -, *, /): ")
num1 = float(input("Digite o primeiro número: "))
num2 = float(input("Digite o segundo número: "))

if op == "+":
    resultado = operacoes.soma(num1, num2)
    utils.exibir_resultado("soma", resultado)
elif op == "-":
    resultado = operacoes.subtracao(num1, num2)
    utils.exibir_resultado("subtração", resultado)
elif op == "*":
    resultado = operacoes.multiplicacao(num1, num2)
    utils.exibir_resultado("multiplicação", resultado)
elif op == "/":
    resultado = operacoes.divisao(num1, num2)
    utils.exibir_resultado("divisão", resultado)
else:
    print("Operação inválida.")
