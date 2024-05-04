palavra_secreta = "banana"
tentativas_restantes = 6
letras_descobertas = ["_"] * len(palavra_secreta)

while tentativas_restantes > 0 and "_" in letras_descobertas:
    print(" ".join(letras_descobertas))
    letra = input("Digite uma letra: ")

    if letra in palavra_secreta:
        print("Acertou!")
        for i in range(len(palavra_secreta)):
            if palavra_secreta[i] == letra:
                letras_descobertas[i] = letra
    else:
        print("Errou!")
        tentativas_restantes -= 1

if "_" not in letras_descobertas:
    print("Parabéns, você venceu!")
else:
    print("Você perdeu! A palavra era:", palavra_secreta)

