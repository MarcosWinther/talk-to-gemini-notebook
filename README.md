# 🎙️ Projeto Assistente de Voz Utilizando Gemini

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Google%20Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white)
![Google Colab](https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)

Este repositório contém um assistente de voz inteligente e minimalista desenvolvido para rodar inteiramente no **Google Colab**. Ele utiliza a capacidade multimodal do **Gemini 2.5 Flash** para ouvir áudios, transcrever o que foi dito e responder via síntese de voz em tempo real.

<br>

## 🎯 Objetivo
O projeto foi desenhado como uma solução de **"arquivo único"** (single file). O objetivo é demonstrar a integração entre APIs de IA multimodal e interfaces de navegador, permitindo que o Gemini processe áudio nativamente sem a necessidade de modelos intermediários de transcrição (como o Whisper), tornando a resposta mais rápida e fluida.

<br>

## 🛠️ Ferramentas e Tecnologias
* **Gemini 2.5 Flash:** O modelo de IA que processa áudio, entende o contexto e gera a resposta.
* **gTTS (Google Text-to-Speech):** Biblioteca responsável por transformar a resposta de texto em fala (.mp3).
* **JavaScript API:** Integrada ao Python para acessar o hardware do microfone através do navegador.
* **Python:** Linguagem base que orquestra o fluxo de dados e os arquivos.

<br>

## 🚀 Como Funciona?
O fluxo foi otimizado para não acumular arquivos desnecessários no ambiente:
1.  **Limpeza:** Antes de cada gravação, o sistema remove arquivos de áudio existentes.
2.  **Captura:** O usuário grava sua pergunta diretamente pelo microfone no notebook.
3.  **Multimodalidade:** O Gemini analisa o áudio bruto, transcreve a pergunta (exibida na tela para o usuário) e gera a resposta.
4.  **Feedback:** A resposta é impressa em texto e reproduzida via áudio automaticamente.

> [!IMPORTANT]
> **Gestão de Arquivos Voláteis:** Todos os áudios (`user_input.wav` e `bot_response.mp3`) são temporários. Eles residem apenas na memória/disco da instância atual do Google Colab e são deletados a cada nova execução para garantir a privacidade e organização.

---

## 📂 Estrutura do Repositório
Focado em simplicidade, o repositório contém apenas o essencial para o funcionamento:

```text
├── 📄 README.md                                          # Documentação do projeto
└── 📄 projeto-assistente-de-voz-utilizando-gemini.ipynb  # Notebook completo com o código
````

<br>

## ⚙️ Configuração Necessária

Para rodar este projeto com sucesso, você precisará configurar sua **API Key**:

1.  Obtenha uma chave gratuita no [Google AI Studio](https://aistudio.google.com/).
2.  No seu Google Colab, clique no ícone de chave (**Secrets**) na barra lateral esquerda.
3.  Adicione um segredo com o nome exato: `GEMINI_KEY`.
4.  Cole sua chave no campo de valor e **ative** o botão "Notebook access".

<br>

## 💡 Destaques Técnicos
* **Resposta Transcritiva:** O código solicita que o Gemini primeiro transcreva o áudio para que o usuário possa validar o que foi entendido pela IA.
* **Filtro de Voz:** O motor de fala ignora a transcrição e vocaliza apenas a resposta do bot, evitando que o assistente repita a sua própria pergunta.
* **Auto-Instalação:** O notebook verifica e instala automaticamente as bibliotecas ausentes (`google-generativeai`, `gTTS`) a cada nova sessão.

<br>

## 👨‍💻 Expert

<p>
    <img 
      align=left 
      margin=10 
      width=80 
      src="https://avatars.githubusercontent.com/u/44624583?v=4"
    />
    <p>&nbsp&nbsp&nbspMarcos Winther<br>
    &nbsp&nbsp&nbsp
    <a href="https://github.com/MarcosWinther">
    GitHub</a>&nbsp;|&nbsp;
    <a href="https://www.linkedin.com/in/marcoswinthersilva/">LinkedIn</a>
    </p>
</p>
<br/><br/>

---

⌨️ com 💜 por [Marcos Winther](https://github.com/MarcosWinther)