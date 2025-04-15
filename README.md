# Chatbot simples com Python

def responder(pergunta):
    pergunta = pergunta.lower()
    
    if "oi" in pergunta or "olá" in pergunta:
        return "Olá! Como posso ajudar você hoje?"
    elif "nome" in pergunta:
        return "Eu sou um chatbot criado em Python!"
    elif "tempo" in pergunta:
        return "Eu não tenho acesso ao clima, mas espero que esteja um dia bonito!"
    elif "adeus" in pergunta or "tchau" in pergunta:
        return "Até logo! Foi bom conversar com você."
    else:
        return "Desculpe, não entendi. Pode perguntar de outra forma?"

# Loop principal
print("Bem-vindo ao Chatbot! Digite 'sair' para encerrar.")
while True:
    user_input = input("Você: ")
    if user_input.lower() == "sair":
        print("Chatbot: Tchau! Até a próxima.")
        break
    resposta = responder(user_input)
    print("Chatbot:", resposta)
