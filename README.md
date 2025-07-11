# README - Chatbot Gemini AI com Suporte a Imagens
Este documento explica o código de um chatbot simples desenvolvido em HTML, CSS (com Tailwind CSS) e JavaScript puro, que se integra à API Gemini AI e permite o envio de mensagens de texto e imagens.

## Visão Geral
Este projeto demonstra como criar uma interface de chatbot interativa que pode se comunicar com um modelo de linguagem grande como o Gemini AI. A funcionalidade principal inclui o envio de mensagens de texto e a capacidade de anexar imagens para que a IA possa interpretá-las e responder.

## Funcionalidades
- Interface Amigável: Design limpo e responsivo, utilizando Tailwind CSS para uma estilização moderna e adaptável a diferentes tamanhos de tela.

- Comunicação em Tempo Real: Exibição dinâmica de mensagens do usuário e respostas da IA.

- Suporte a Imagens: Permite que o usuário faça upload de imagens, que são convertidas para Base64 e enviadas junto com a mensagem de texto para a API Gemini.

- Integração com a API Gemini AI: Utiliza a API gemini-2.0-flash para processar as interações do chat e gerar respostas.

- Indicador de Carregamento: Exibe uma mensagem "Chatbot está digitando..." enquanto aguarda a resposta da IA.

- Histórico de Conversa: Mantém um histórico da conversa para fornecer contexto à IA.

## Como Usar
Para executar este chatbot, siga os passos abaixo:

1. Salve o Código: Copie todo o código HTML fornecido e salve-o em um arquivo com a extensão .html (por exemplo, chatbot.html).

2. Abra no Navegador: Abra o arquivo .html em qualquer navegador web moderno.

3. Interaja:

    - Digite sua mensagem na caixa de texto na parte inferior.

    - Pressione Enter ou clique no botão "Enviar" para enviar sua mensagem.

    - Para anexar uma imagem, clique no botão "Anexar Imagem", selecione um arquivo de imagem do seu computador e, em seguida, clique em "Enviar" (com ou sem texto adicional).

Você pode limpar a imagem selecionada clicando no botão "Limpar Imagem" ao lado da pré-visualização da imagem.

## Detalhes Técnicos
- HTML: Estrutura básica da página e dos elementos do chatbot.

- CSS (Tailwind CSS): Utilizado para estilização rápida e responsiva. O CDN do Tailwind é incluído diretamente no HTML.

- JavaScript:
    - Manipula a interface do usuário (adicionar mensagens, mostrar/ocultar indicadores).

    - Lê arquivos de imagem e os converte para o formato Base64.

    - Faz chamadas fetch assíncronas para a API Gemini AI.

    - Gerencia o histórico da conversa (chatHistory) para manter o contexto.

    - A apiKey para a API Gemini é deixada vazia (const apiKey = "";), pois o ambiente Canvas a fornece automaticamente em tempo de execução.

## Próximos Passos (Sugestões de Melhoria)
- Integração com Angular: Este código pode ser a base para um componente Angular. Você precisaria migrar o HTML para o template do componente, o JavaScript para o arquivo TypeScript do componente (usando HttpClient para as chamadas API e ngModel para data binding), e gerenciar o estado da aplicação com as ferramentas do Angular.

- Persistência de Dados: Implementar o salvamento do histórico de chat (por exemplo, em um banco de dados como o Firestore) para que as conversas possam ser retomadas.

- Autenticação de Usuários: Adicionar um sistema de autenticação para identificar usuários e gerenciar conversas individuais.

- Melhorias na UI/UX: Adicionar mais animações, feedback visual aprimorado e opções de formatação para as mensagens.

- Tratamento de Erros: Implementar um tratamento de erros mais robusto para as chamadas da API e exibir mensagens mais amigáveis ao usuário em caso de falha.