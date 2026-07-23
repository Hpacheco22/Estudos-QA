# Estudos-QA Saucedemo
CT001.
**titulo:** teste login de usuário com credenciais válidas.
**passos:** 
1. entrar no site 
2. digitar seu login  "standard_user" no campo usuário
3. digitar "secret_sauce" no campo senha
4. clicar em continuar

**Resultado esperado:** ser direcionado a pagina correspondente "saucedemo",  com os produtos listados

**status:** passou.

---
CT002. 
**Titulo:** teste de login com credenciais inválidas.  
**passos:** 
1. entrar no site
2. digitar "usuário_errado" no campo de usuário
3. digitar "senha_errada" no campo de senha
4. clicar em login

 **resultado esperado:** receber a mensagem informando que login e senha estão errados e permanecer na pagina em questão
 
 **status:** passou.

 ---
CT003 
**Titulo:** teste de login com o campo de senha vazia.  
**Passos:** 
1. entrar no site
2. digitar login "standard_user"
3. não digitar nada no campo senha
4. clicar em  login
  
**Resultado esperado:** receber mensagem informando que algum dos campos obrigatórios está em branco

**Status:** passou




## Scripts Python

```python


Bug = {
    "titulo": "Checkout finaliza sem solicitar forma de pagamento",
    "passos": [
        "Acessar saucedemo.com e fazer login",
        "Adicionar produto ao carrinho",
        "Preencher nome, sobrenome e CEP",
        "Clicar em continue e Finish"
    ],
    "Resultado_atual": "Pedido confirmado sem solicitação de pagamento",
    "Resultado_esperado": "Sistema deve solicitar forma de pagamento antes de confirmar",
    "Severidade": "Crítica"
}

print("=== BUG REPORT ===")
print("Titulo", bug["titulo"])
print("Severidade", bug["Severidade"])
print("Resultado atual", bug["Resultado_atual"])
print("Resultado esperado", bug["Resultado_esperado"])
print("Passos:")
for passo in bug["passos"]:
    print("-", passo)

bug2 = {
    "titulo": "Compra finaliza sem solicitar endereço",
    "passos": [
        "Acessar saucedemo.com e fazer login",
        "Adicionar produto ao carrinho",
        "Preencher nome, sobrenome e CEP",
        "Clicar em continue e Finish"
    ],
    "Resultado_atual": "pedido confirmado sem solicitação de endereço",
    "Resultado_esperado": "O sistema deve solicitar o enedere como CEP, rua e numero da residência do cliente antes de confirmar",
    "Severidade": "Alta"
}
print("=== BUG REPORT2 ===")
print("titulo", bug2["titulo"])
print("Severidade", bug2["Severidade"])
print("Resultado atual", bug2["Resultado_atual"])
print("Resultado esperado", bug2["Resultado_esperado"])
print("passos:")

for passo in bug2["passos"]:
    print("-", passo)


bug3 = {
    "titulo": "A compra é finalizada sem prazo de entrega",
    "passos": [
        "Acessar saucedemo.com e fazer login",
        "adicionar produto escolhido ao carrinho",
        "preencher nome, sobrenome e CEP",
        "Clicar em continue e finish"
    ],
    "Resultado_atual": "Compra finalizada sem pedir ou informar prazo de entrega",
    "Resultado_esperado": "Antes da confirmação da compra, o sistema deve exibir o prazo estimado de entrega e permitir que o cliente escolha uma data disponível para receber o produto.",
    "Severidade": "Baixa"
}
print("=== BUG REPORT3 ===")
print("titulo", bug3["titulo"])
print("Severidade", bug3["Severidade"])
print("Resultado atual", bug3["Resultado_atual"])
print("Resultado esperado", bug3["Resultado_esperado"])
print("passos:")

for passo in bug3["passos"]:
    print("-", passo)
'''


