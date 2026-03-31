# ClickEnter Utilities

Extensão para Tampermonkey projetada para otimizar o fluxo de atendimento no PipeRun (ClickEnter), fornecendo ferramentas de monitoramento, automação com inteligência artificial e organização de dados.

## Funcionalidades Principais

### Monitoramento de TMA (Tempo Médio de Atendimento)
- Cálculo automático do tempo de permanência em cada atendimento.
- Indicadores visuais na barra lateral: borda laranja para alerta (padrão 35 min) e borda vermelha para crítico (padrão 60 min).
- Notificações nativas do navegador e alertas sonoros quando um atendimento excede 1 hora.

### Relato Automatizado com I.A.
- Geração de resumos técnicos de atendimento utilizando Gemini (Google) ou ChatGPT (OpenAI).
- O algoritmo prioriza anotações feitas pelo atendente e utiliza o histórico do chat como contexto secundário.
- Saída formatada em primeira pessoa, pronta para ser copiada para o sistema de CRM.

### Cronômetro Individual por Cliente
- Configuração de timers personalizados para cada aba de atendimento.
- Notificações sonoras e visuais ao término do tempo configurado.
- Persistência do estado do timer ao alternar entre diferentes atendimentos.

### Gestão de Lembretes e Notas
- Campo de anotações rápidas vinculadas especificamente ao cliente em atendimento.
- Dados salvos localmente, servindo de base para a geração do relato por I.A.

### Mensagens Prontas
- Repositório de textos frequentes para resposta rápida.
- Atalhos de cópia com um clique para agilizar a comunicação.

### Interface Adaptável
- Painel lateral expansível com dois modos de visualização:
  - **Overlay**: Painel flutuante sobre a interface.
  - **Integrated**: Integração direta ao lado do chat, redimensionando a área principal.
- Largura do painel ajustável manualmente.

## Guia de Instalação e Configuração

### 1. Instalação do Tampermonkey
O ClickEnter Utilities requer um gerenciador de scripts de usuário para funcionar. Recomendamos o Tampermonkey. Escolha a versão correspondente ao seu navegador:

- **Google Chrome**: [Instalar via Chrome Web Store](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)
- **Microsoft Edge**: [Instalar via Edge Add-ons](https://microsoftedge.microsoft.com/addons/detail/tampermonkey/iikmkjmpaadaobahmlepeloendndfphd)
- **Mozilla Firefox**: [Instalar via Firefox Add-ons](https://addons.mozilla.org/pt-BR/firefox/addon/tampermonkey/)
- **Opera**: [Instalar via Opera Add-ons](https://addons.opera.com/en/extensions/details/tampermonkey-beta/)

### 2. Configurações de Desenvolvedor
Devido a recentes políticas de segurança, especialmente em navegadores baseados no Chromium (como Chrome e Edge), é necessário habilitar permissões adicionais para a execução de scripts.

**Ativando o Modo do Desenvolvedor no Navegador:**
1. Abra a página de gerenciamento de extensões do seu navegador (digite `chrome://extensions/` ou `edge://extensions/` na barra de endereços).
2. Localize a opção **Modo do desenvolvedor** (geralmente no canto superior direito) e ative a chave correspondente.

**Habilitando UserScripts no Tampermonkey:**
1. Clique no ícone do Tampermonkey na barra superior e selecione **Painel de Controle** (Dashboard).
2. Acesse a aba superior de **Configurações** (Settings).
3. Na primeira seção da tela, altere o **Modo de Configuração** (Config mode) para **Avançado** (Advanced).
4. Em navegadores que exigem uma validação extra, role a página até a seção de segurança ou proteção de scripts e certifique-se de que a injeção ou execução de usuárioscripts não esteja restrita pelas configurações de segurança nativas do Tampermonkey.

### 3. Adicionando o ClickEnter Utilities
Com o ambiente devidamente preparado, basta adicionar o script em si:
1. Abra o arquivo `ClickEnter-Utilities.user.js` em um editor de texto e copie todo o seu conteúdo.
2. Clique no ícone do Tampermonkey no navegador e em seguida selecione **Adicionar novo script**.
3. Uma nova aba contendo um editor de código aparecerá. Apague por completo qualquer conteúdo inicial exibido ali.
4. Cole todo o código copiado do `ClickEnter-Utilities.user.js`.
5. Salve a modificação acessando a aba **Arquivo** ou **File** e selecionando **Salvar** (se preferir, use o atalho `Ctrl + S`).

O script já se encontrará ativo na sua lista principal do Tampermonkey e iniciará sua execução imediatamente assim que você recarregar a página do atendimento.

### Sistema de Atualização (WIP)
A extensão apresenta um verificador de versão integrado que consulta o repositório oficial no GitHub.
- Quando detectada uma nova versão, surgirá a indicação para "ATUALIZAR" no cabeçalho do painel.
- O procedimento de atualização é conduzido de forma nativa pelo Tampermonkey através de um simples clique nesse botão.

## Configuração Técnico-Operacional

Acesse o ícone de engrenagem no painel para configurar:
- Chaves de API (Gemini ou OpenAI) para os recursos de I.A.
- Limites de tempo para alertas e avisos críticos de TMA.
- Preferências de interface e largura padrão do painel.
