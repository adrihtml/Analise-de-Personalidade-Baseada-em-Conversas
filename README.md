# Analise de Personalidade Baseada em Conversas
Este código analisa mensagens de texto (como as de um chat do WhatsApp) para mapear traços de personalidade com base no uso de palavras-chave e, em seguida, gera um resumo que define a personalidade do autor das mensagens filtradas.
O intuito desse código foi mapear uma personalidade específica para treinar uma IA generativa, para agir como tal. Realmente foi um desafio e no projeto final acabei utilizando um pouco deste prompt para elaborar o código atual, que ainda não está finalizado. (Em breve mais sobre EVP)

Abaixo estão os principais pontos explicados:

# Mapeamento de Personalidade:

## A função mapear_personalidade analisa uma lista de mensagens, verificando a frequência de palavras associadas a traços específicos:

Emocional: Palavras que indicam sentimentos;

Racional: Palavras relacionadas a lógica e planejamento;

Positivo e Negativo: Indicadores de otimismo ou pessimismo;

Confiante: Palavras que transmitem segurança e determinação;

Neutro: Quando nenhuma palavra-chave específica é encontrada.

# Geração de Prompt de Personalidade:

A função **gerar_prompt_personalidade** usa os traços contados para criar um texto descritivo, destacando características predominantes na comunicação.

# Processamento de Mensagens:
A função **processar_mensagens** lê um arquivo de texto contendo mensagens de um chat, filtra as mensagens por um nome ou termo específico, remove as informações de data/hora e processa o conteúdo com as funções anteriores.

# Exemplo de Documento:

Você pode utilizar uma conversa exportada do Whatsapp. Para melhores resultados, indico utilizar conversas maiores. 

# Exemplo de Saída:

![image](https://github.com/user-attachments/assets/60d7878a-b747-4ab6-8741-093e58793623)


# Adaptação para Preenchimento de Dados
Aqui está como você pode configurar para preencher os campos necessários:

    # Preencha os dados abaixo:
    arquivo_txt = input("Digite o caminho do arquivo de texto com as mensagens: ")  # Exemplo: '/content/Conversa.txt'
    filtro_de_busca = input("Digite o nome ou termo para filtrar mensagens: ")  # Exemplo: 'Adri'

    # Processa as mensagens com os dados fornecidos
    prompt_resultante = processar_mensagens(arquivo_txt, filtro_de_busca)
    print(prompt_resultante)

# Dados para Preencher
1. Caminho do Arquivo: Insira o caminho completo do arquivo de texto contendo as mensagens.
2. Filtro de Busca: Insira o termo ou nome que será usado para filtrar as mensagens.

Por fim, agradeço a leitura dos pontos citados. Espero que esteja claro como utilizar.

Fico á disposição em qualquer dúvida referente á este reporitório. Você pode falar comigo pelo e-mail: adri.bill.cam@gmail.com
