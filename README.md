# Analisador-de-Telefone
Analisador de Telefone

- Criando um programa que receba um telefone e verifica se ele é um telefone real brasileiro. O programa ira conseguir tratar espaços em branco, parênteses, existência de um 9º dígito no número ou não, existência de DDD ou não e de ira obrigar o usuário a inserir o código do País (+55)

Válidos:<br>
"+55 21 9799999999"<br>
"+55 21 799999999 "<br>
"+55 (21)79999-9999"<br>
"+5521799999999"<br>

telefone = input("Insira seu telefone no formato +55XX999999999")

telefone = telefone.replace(" ", "").replace("(", "").replace(")", "").replace("-", "")
if telefone[:3]!="+55":
    print("Esse telefone não é brasileiro ou foi inserido no formato errado")
else:
    if len(telefone)!=13 and len(telefone)!=14:
        print("Esse telefone não é brasileiro ou foi inserido no formato errado")
    else:
        print("Telefone válido:", telefone)
