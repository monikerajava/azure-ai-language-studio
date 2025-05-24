# Explorando Serviços de IA no Azure AI Foundry

Este resumo detalha como utilizar os serviços de **Azure AI Language** e **Azure AI Speech** dentro do portal **Azure AI Foundry**, uma plataforma da Microsoft para criar aplicações inteligentes.

O conteúdo é baseado em dois serviços: um sobre Análise de Texto e outro sobre Exploração de Fala, ambos no Azure AI Foundry portal.

## O que é Azure AI Foundry portal?

O Azure AI Foundry portal é a plataforma da Microsoft onde você pode criar aplicações inteligentes. Ele serve como um local para explorar e utilizar diversos serviços de IA, como Language e Speech.

Para começar, é necessário **criar um projeto** dentro do portal.

### Como Criar um Projeto

1.  Abra o portal **Azure AI Foundry** em `https://ai.azure.com` e faça login com suas credenciais Azure. Feche quaisquer dicas iniciais.
2.  Navegue para `https://ai.azure.com/managementCenter/allResources`.
3.  Selecione **Create**.
4.  Escolha a opção para criar um *new AI hub resource*.
5.  No assistente "Create a project", insira um nome válido para o seu projeto.
6.  Se um hub existente for sugerido, selecione a opção para criar um *new*.
7.  Expanda "Advanced options" para especificar as seguintes configurações:
    *   **Subscription**: Sua assinatura Azure.
    *   **Resource group**: Crie ou selecione um grupo de recursos.
    *   **Region**: Selecione uma das localizações disponíveis, como East US, France Central, Korea Central, West Europe, ou West US.
8.  Aguarde a criação do seu projeto e hub.
9.  Ao final, você será levado para uma página de "Overview" (Visão Geral) com os detalhes do projeto.

Após a criação do projeto, você pode acessar os **Playgrounds** no menu do lado esquerdo para experimentar as capacidades dos serviços de IA. Estão disponíveis o **Language playground** e o **Speech playground**.

## Serviço Azure AI Language

**Natural Language Processing (NLP)** é um ramo da IA que lida com linguagem escrita e falada. O Azure AI Language service, que inclui **Text Analytics**, oferece diversas capacidades de NLP para extrair significado semântico de texto ou fala.

Exemplos de uso incluem analisar avaliações de clientes para extrair entidades nomeadas, identificar frases-chave, resumir texto e analisar sentimento.

No Language playground, você pode explorar algumas dessas capacidades:

### 1. Extrair Entidades Nomeadas

*   **O que são:** Palavras que descrevem pessoas, lugares e objetos com nomes próprios.
*   **Como acessar:** No Language playground, selecione **Extract information**, e depois **Extract named entities**.
*   **Exemplo:** Foi utilizada uma avaliação de hotel de "The Royal Hotel, London".
*   **Output:** Na seção "Details", as entidades extraídas vêm com informações adicionais como **tipo** (e.g., Localidade, Organização) e **confidence scores** (pontuações de confiança). A pontuação de confiança indica a probabilidade de que o tipo identificado pertença àquela categoria.

### 2. Extrair Frases-Chave

47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
64
65
66
67
68
69
70
71
72
73
74
75
76
77
78
79
80
81
82
83
84
85

*   **O que são:** As peças de informação mais importantes em um texto.
*   **Como acessar:** No Language playground, selecione **Extract information**, e depois **Extract key phrases**.
*   **Exemplo:** Foi utilizada uma avaliação de hotel diferente, também sobre "The Royal Hotel, London".
*   **Output:** A seção "Details" mostra as diferentes frases extraídas. Essas frases devem ser as que mais contribuem para o significado do texto.

### 3. Resumir Texto

*   **O que é:** Obter um resumo conciso do texto.
*   **Como acessar:** No Language playground, selecione **Summarize information**, e depois **Summarize text**.
*   **Exemplo:** Foi utilizada uma avaliação de hotel sobre "The Lombard Hotel, San Francisco".
*   **Output:** A seção "Details" fornece um *Extractive summary* (resumo extrativo), apresentando **rank scores** para as frases mais salientes (importantes).

## Serviço Azure AI Speech

O **Azure AI Speech service** permite transcrever fala em texto e texto em fala audível. Pode ser usado para criar aplicações que transcrevem notas de reunião ou geram texto a partir de gravações.

No Speech playground, você pode experimentar as capacidades de fala, como *speech to text*.

### Explorar Speech to Text

*   **O que é:** O processo de converter áudio falado em texto escrito.
*   **Como acessar:** No Speech playground, role para baixo e selecione **Real-time transcription** sob "Try out Speech capabilities". Isso o levará ao Speech Playground.
*   **Exemplo:** Foi necessário baixar um arquivo zip (`speech.zip`) contendo um arquivo de áudio chamado **WhatAICanDo.m4a** a partir de um link fornecido (`https://aka.ms/mslearn-speech-files`).
*   **Processo:** Sob "Upload files", você usa o botão "Browse files" para selecionar e carregar o arquivo de áudio **WhatAICanDo.m4a**.
*   **Output:** O serviço Speech **transcreve e exibe o texto em tempo real**. Se seu computador tiver áudio, você pode ouvir a gravação enquanto o texto é transcrito. O output deve ter reconhecido e transcrito o áudio com sucesso. Você pôde ver a transcrição de texto sendo gerada conforme o arquivo de áudio era reproduzido.

## Limpeza de Recursos

Para evitar custos desnecessários, é importante excluir os recursos criados se você não pretende fazer mais exercícios.

1.  Abra o **Azure portal** em `https://portal.azure.com`.
2.  Selecione o grupo de recursos que contém os recursos que você criou.
3.  Selecione os recursos que deseja excluir.
4.  Selecione **Delete** e então **Yes** para confirmar. Os recursos são então excluídos.

## Saiba Mais

Os documentos mencionam que os exercícios demonstram apenas algumas das muitas capacidades dos serviços. Para aprender mais sobre o que você pode fazer com estes serviços, você pode consultar as páginas dedicadas ao **Language service** e ao **Speech service**.

https://aka.ms/ai900-speech

https://aka.ms/ai900-text-analysis
***
