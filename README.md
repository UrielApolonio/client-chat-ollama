# 💬 Chat Ollama (client) By Uriel

<p align="center">
  <img src="https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white" alt="Ollama Badge">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5 Badge">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3 Badge">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript Badge">
  <img src="https://img.shields.io/badge/Open%20Source-30A3DC?style=for-the-badge&logo=opensourceinitiative&logoColor=white" alt="Open Source Badge">
</p>

Uma interface de chat simples e eficiente para interagir com um servidor de Inteligência Artificial [Ollama](https://ollama.ai/). Desenvolvido em HTML, CSS e JavaScript puro, este projeto oferece uma maneira prática de conversar com seus modelos de linguagem locais, incluindo suporte para anexos de arquivos (texto e imagem) e configurações avançadas de geração de texto.

---

## ✨ Funcionalidades Principais

Este chat foi projetado para otimizar sua interação com modelos Ollama, oferecendo um controle detalhado sobre as configurações e a entrada de dados:

*   **Conexão Flexível:** A URL da API Ollama pode ser facilmente configurada nas definições (`http://localhost:11434/api/chat` por padrão), permitindo a conexão a diferentes instâncias do Ollama.
*   **Seleção Dinâmica de Modelos:** O chat consulta automaticamente seu servidor Ollama para listar todos os modelos disponíveis, permitindo que você selecione e alterne entre eles de forma intuitiva.
*   **Configurações de Geração Avançadas:** Controle fino sobre como o modelo gera suas respostas:
    *   **Tamanho do Contexto (`num_ctx`):** Ajuste o limite máximo de tokens para o prompt de entrada, influenciando a "memória" do modelo.
    *   **Comprimento Máximo da Resposta (`num_predict`):** Defina o número máximo de tokens para as respostas geradas pelo modelo.
    *   **Prompt do Sistema (`system`):** Personalize as instruções iniciais que guiam o comportamento e a persona do modelo.
    *   **Memória de Contexto:** Um controle para ativar ou desativar o uso do histórico da conversa, permitindo que o modelo mantenha ou ignore o contexto de interações anteriores.
*   **Presets de Geração:** Alterne rapidamente entre conjuntos de parâmetros otimizados para diferentes tipos de interação:
    *   **"Conversação":** Ideal para diálogos fluídos e naturais.
    *   **"Programação":** Otimizado para geração e depuração de código.
    *   **"Criativo":** Favorece respostas mais imaginativas e originais (ideal para brainstorming).
    *   **"Padrão do Modelo":** Reseta os parâmetros para as configurações originais do modelo Ollama selecionado.
*   **Anexos de Arquivo:**
    *   **Documentos:** Suporte para anexar arquivos de texto (`.txt`, `.csv`) e PDFs. O conteúdo dos PDFs é automaticamente extraído para ser analisado pelo modelo.
    *   **Imagens:** Permite anexar imagens (`.png`, `.jpeg`, `.gif`, `.webp`) para interagir com modelos multimodais (como o `llava`).
    *   É possível anexar até 5 arquivos por vez, desde que sejam da mesma categoria (texto ou imagem).
*   **Interface Intuitiva:**
    *   Exibição clara do histórico de mensagens do usuário e do bot, renderizadas com formatação Markdown para melhor legibilidade.
    *   Realce de sintaxe para blocos de código e JSON nas respostas do bot.
    *   Barra de status que fornece feedback em tempo real sobre a conexão e as operações.
    *   Botão "Copiar" para copiar facilmente as respostas formatadas do bot para a área de transferência.
*   **Ferramentas de Visualização:**
    *   **"Ver Último Envio":** Inspecione o JSON exato que foi enviado para a API Ollama na última requisição, útil para depuração.
    *   **"Informações do Modelo Selecionado":** Obtenha detalhes técnicos e metadados sobre o modelo Ollama que está atualmente selecionado, diretamente do seu servidor Ollama.
*   **Gerenciamento do Chat:** Botão para limpar todo o histórico de mensagens e redefinir as configurações para os padrões.
*   **Design Responsivo:** A interface se adapta bem a diferentes tamanhos de tela, proporcionando uma experiência consistente em desktops e dispositivos móveis.
*   **Persistência de Configurações:** Suas configurações preferidas são salvas localmente no navegador, carregando automaticamente na próxima vez que você usar o chat.

---

## �� Como Usar

Para começar a interagir com seus modelos Ollama através desta interface de chat, você precisa ter o Ollama instalado e rodando.

### Pré-requisitos

*   **Ollama:** Certifique-se de ter o [Ollama](https://ollama.ai/) instalado e em execução em seu sistema, com um ou mais modelos de linguagem baixados.

### Execução

1.  **Baixe o arquivo `index.html`:** Faça o download do arquivo `index.html` para uma pasta de sua escolha em seu computador.
2.  **Abra o arquivo no navegador:** Simplesmente abra o arquivo `index.html` usando qualquer navegador web moderno de sua preferência (Google Chrome, Mozilla Firefox, Microsoft Edge, Safari, etc.).
3.  **Configuração Inicial:**
    *   Por padrão, o chat tentará se conectar à API Ollama em `http://localhost:11434/api/chat`. Se a sua instalação do Ollama estiver em um endereço diferente, clique no botão `⚙️ Configurações` (canto superior direito) e ajuste a `URL da API Ollama` conforme necessário.
    *   Após a conexão, o menu `Seleção de Modelo` será preenchido automaticamente com os modelos disponíveis no seu servidor Ollama. Escolha o modelo com o qual deseja conversar.
4.  **Inicie a Conversa:** Digite sua mensagem na caixa de texto na parte inferior da tela e pressione `Enter` ou clique no botão `Enviar`.

### Anexando Arquivos

1.  Para anexar arquivos à sua mensagem, clique no botão `Anexar` (📎) ao lado da caixa de texto.
2.  Uma janela modal será exibida, onde você pode arrastar e soltar arquivos ou clicar para navegar e selecioná-los.
3.  Os arquivos selecionados aparecerão na lista. Clique em `Limpar Arquivos Anexados` se precisar remover algum.
4.  Após anexar, os arquivos serão enviados junto com a próxima mensagem que você enviar.

---

## 🛠️ Tecnologias Utilizadas

*   **HTML5:** A estrutura fundamental da página.
*   **CSS3:** Estilização completa da interface, incluindo o uso de variáveis CSS para facilitar a personalização de cores.
*   **JavaScript:** Toda a lógica interativa do chat, comunicação com a API Ollama, manipulação do DOM e processamento de arquivos.
*   **[Marked.js](https://marked.js.org/):** Uma biblioteca JavaScript para renderizar respostas formatadas em Markdown.
*   **[PDF.js](https://mozilla.github.io/pdf.js/):** Uma biblioteca da Mozilla para leitura e extração de texto de arquivos PDF diretamente no navegador.

---

## 🤝 Contribuição

Este projeto é de código aberto! Sua contribuição é bem-vinda para torná-lo ainda melhor. Se você tem ideias para novas funcionalidades, identificou um bug ou deseja melhorar o código, por favor, siga os passos abaixo:

1.  Faça um **Fork** deste repositório.
2.  Crie uma nova `branch` para suas alterações: `git checkout -b feature/nome-da-sua-feature` ou `git checkout -b bugfix/correcao-de-bug`.
3.  Implemente suas mudanças e faça commits descritivos.
4.  Envie sua `branch` para o seu repositório forked: `git push origin feature/nome-da-sua-feature`.
5.  Abra um **Pull Request** para o repositório original, descrevendo claramente suas alterações.

Sua colaboração é muito apreciada!

---

## 📄 Licença

Este projeto está licenciado sob a Licença MIT. Para mais detalhes, consulte o arquivo [LICENSE](LICENSE) neste repositório.

---

## 🧑‍💻 Autor

Desenvolvido por Uriel Gusmão Apolônio.

---
