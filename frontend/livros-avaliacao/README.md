# Módulo Frontend: Livros e Avaliações

Este diretório contém o código frontend responsável pelas funcionalidades de visualização, busca, detalhamento e avaliação de mangás dentro do Sistema Web de Comentários e Avaliação de Mangás "NextPage". Este módulo é desenvolvido e mantido por Cassio.

## Descrição Geral

Este módulo do frontend abrange todas as interfaces de usuário relacionadas à interação com os mangás e suas avaliações. Isso inclui:

* Listagem e exibição de mangás.
* Funcionalidades de busca por mangás.
* Visualização detalhada de informações sobre um mangá específico.
* Exibição de comentários e avaliações existentes.
* Funcionalidade para usuários adicionarem novos comentários e avaliações.

O objetivo principal é fornecer uma experiência intuitiva e responsiva para os usuários navegarem pelo catálogo de mangás e compartilharem suas opiniões.

## Configuração e Execução (Modo Isolado - se aplicável)

*(Esta seção pode variar dependendo de como o frontend é estruturado. Se for uma Single Page Application (SPA) monolítica, pode não ser fácil rodar apenas esta parte isoladamente. Adapte conforme a realidade do projeto.)*

Se este módulo puder ser desenvolvido ou testado isoladamente (por exemplo, usando Storybook para componentes, ou um servidor de desenvolvimento local que simule as APIs):

1.  **Instalar dependências:**
    ```bash
    cd ../../  # Volte para o diretório raiz do frontend (nextpage/frontend)
    npm install # Ou yarn install, dependendo do gerenciador de pacotes principal do frontend
    cd livros-avaliacao # Volte para este diretório
    ```
2.  **Rodar servidor de desenvolvimento local (Exemplo usando um script no `package.json` global ou local):**
    ```bash
    # Exemplo: se houver um script específico para este módulo no package.json global
    npm run dev:livros-avaliacao
    # Ou se você configurou um servidor local aqui (menos comum em SPA monolíticas)
    # npm start
    ```
3.  **Acessar no navegador:** Abra seu navegador em `http://localhost:[PORTA]` (substitua `[PORTA]` pela porta configurada).

Se não for possível rodar isoladamente, descreva como rodar a aplicação frontend completa:

1.  **Navegue para o diretório raiz do frontend:**
    ```bash
    cd ../../  # Volte para o diretório raiz do frontend (nextpage/frontend)
    ```
2.  **Instale as dependências (se ainda não o fez):**
    ```bash
    npm install # Ou yarn install
    ```
3.  **Inicie o servidor de desenvolvimento frontend:**
    ```bash
    npm start # Ou o comando configurado no package.json principal
    ```
4.  **Acesse a aplicação no navegador:** Abra `http://localhost:[PORTA]` e navegue até as páginas relacionadas a mangás e avaliações.

## Dependências Específicas

Este módulo utiliza as dependências globais configuradas no `package.json` principal do diretório `/frontend`.

*(Liste aqui quaisquer bibliotecas ou frameworks específicos que **apenas** este módulo utiliza, se houver. Por exemplo, uma biblioteca de sliders específica para a listagem, ou uma biblioteca de avaliação por estrelas.)*

-   `nome-da-dependencia-especifica`: Descrição breve do que faz. (Instalada via `npm install nome-da-dependencia-especifica` no diretório `/frontend` ou neste diretório, dependendo de como as dependências são gerenciadas).

## Estrutura Interna

A organização dos arquivos dentro deste diretório (`/frontend/livros-avaliacao`) segue a seguinte estrutura: