# Frontend - Livros e Avaliações

Desenvolvido por Cassio, este diretório contém o código frontend responsável pela seção de Livros e Avaliações do sistema NextPage. ele abrange a visualização da lista de mangás, páginas de detalhes individuais de mangás, e a funcionalidade de adicionar e visualizar avaliações.

As principais responsabilidades deste módulo incluem:
* Transcrever o design/protótipo em código HTML, CSS e JavaScript.
* Implementar a interface do usuário para exibir informações de mangás e avaliações.
* Capturar a interação do usuário (cliques, envios de formulários de avaliação, etc.).
* Integrar com as APIs de backend para obter e enviar dados relacionados a mangás e avaliações.

## Configuração e Execução Local

**Pré-requisitos:**

* Python 3 instalado (Verifique executando `python --version` ou `python3 --version` no seu terminal/Prompt de Comando/PowerShell). Se não tiver, baixe e instale do site oficial do Python.
* Node.js e npm instalados (Verifique executando `npm --version`). Necessário para gerenciar dependências frontend.

**Passos:**

1.  **Navegue até o diretório deste módulo:**
    Abra seu terminal (Git Bash, Prompt de Comando ou PowerShell) e vá para o diretório `frontend/livros-avaliacao` dentro do seu repositório clonado:
    ```bash
    cd nextpage/frontend/livros-avaliacao
    ```

2.  **Instale as dependências:**
    Se este módulo possuir dependências listadas no `package.json` que não são globais ao frontend, instale-as:
    ```bash
    npm install
    ```

3.  **Inicie um servidor web local usando Python 3:**
    Dentro do diretório `frontend/livros-avaliacao`, execute o seguinte comando para iniciar um servidor HTTP simples que servirá os arquivos estáticos:
    ```bash
    python -m http.server 8000
    ```
    ou (dependendo da sua instalação Python)
    ```bash
    python3 -m http.server 8000
    ```

4.  **Acesse no Navegador:**
    Abra seu navegador web e vá para `http://localhost:8000`. Você deverá ver a página de índice (geralmente `index.html` se existir na raiz deste diretório ou a listagem dos arquivos). Navegue para a página específica que você está desenvolvendo dentro de `/pages`. Por exemplo, se tiver um `pages/lista-mangas.html`, acesse `http://localhost:8000/pages/lista-mangas.html`.

**Desenvolvimento com VS Code:**

* Abra a pasta `nextpage` no VS Code (`File > Open Folder`).
* Utilize o terminal integrado do VS Code (`View > Terminal`) para executar os comandos `cd` e `npm install`.

## Dependências Específicas

Este módulo frontend utiliza algumas bibliotecas e ferramentas para facilitar o desenvolvimento e a comunicação com o backend. As dependências são gerenciadas através do `package.json` neste diretório.

* **Dependencies:**
    * `axios`: Uma biblioteca cliente HTTP baseada em Promises para o navegador e Node.js. Usada para fazer requisições assíncronas (GET, POST, etc.) às APIs do backend para obter dados de mangás e avaliações e enviar novas avaliações.

* **Dev Dependencies:**
    * `eslint`: Um linter plugável para identificar e reportar padrões encontrados em código ECMAScript/JavaScript. Usado para manter a qualidade do código e forçar padrões de estilo.
    * `prettier`: Um formatador de código opinativo. Usado para garantir um estilo de código consistente e limpo automaticamente, trabalhando em conjunto com o ESLint.
    * `live-server` (Opcional, se você o instalou): Um pequeno servidor HTTP com Live Reload. Usado para servir os arquivos estáticos localmente durante o desenvolvimento e ver as mudanças no navegador em tempo real.

Para instalar estas dependências, execute o comando `npm install` dentro deste diretório (`frontend/livros-avaliacao`).

## Estrutura Interna

A organização dos arquivos dentro deste diretório segue a seguinte estrutura lógica:


* **`/src`**: Contém o código JavaScript que orquestra o funcionamento da aplicação, como inicialização de rotas, configuração de eventos globais, etc.
* **`/pages`**: Cada subdiretório ou conjunto de arquivos aqui representa uma "página" ou "tela" distinta na seção de Livros/Avaliação. É onde o layout principal de cada tela é definido em HTML, estilizado em CSS e com a lógica específica daquela tela em JavaScript.
* **`/components`**: Contém blocos menores e reutilizáveis da interface do usuário. Desenvolver componentes modulares aqui facilita a manutenção e evita a duplicação de código HTML/CSS/JS.

## Instruções de Desenvolvimento e Testes

* Ao desenvolver uma nova funcionalidade, procure dividi-la em componentes menores e reutilizáveis dentro de `/components`.
* Para testar visualmente suas alterações em HTML/CSS/JS, use o servidor HTTP local (`python -m http.server 8000`).
* Para testar a integração com o backend, certifique-se de que o servidor backend está rodando e acessível. Você precisará fazer requisições HTTP a partir do seu código JavaScript.
* (Adicionar aqui instruções específicas sobre como rodar testes unitários ou de integração, se forem implementados mais tarde. Ex: `npm test`)

## Integração com o Backend

Este módulo frontend se comunica com o backend (desenvolvido por Guilherme Lobo) através de APIs. A comunicação é baseada em requisições HTTP (GET, POST, PUT, DELETE) geralmente no formato REST.

* **APIs Utilizadas:**
    * `GET /api/mangas`: Para obter a lista de todos os mangás.
    * `GET /api/mangas/{id}`: Para obter detalhes de um mangá específico.
    * `GET /api/mangas/{id}/avaliacoes`: Para obter as avaliações de um mangá específico.
    * `POST /api/mangas/{id}/avaliacoes`: Para enviar uma nova avaliação para um mangá.

* **Formato dos Dados:**
    A comunicação com o backend utiliza o formato JSON (JavaScript Object Notation) para troca de dados.
    ---