# zourmat.github.io

# Desenvolvimento e organização de projeto de site estático utilizando Jekyll e GitHub Pages
<details> 
    <summary>Clique para expandir</summary>
    O Jekyll é um gerador de sites estáticos que usa arquivos de texto simples, como Markdown e HTML, para criar um site completo. Aqui está um resumo de como os arquivos funcionam no repositório com Jekyll:

    Estrutura do Repositório Jekyll

    Arquivo _config.yml:

    Este arquivo de configuração contém as configurações principais do seu site, como o título, o tema, plugins, etc.

    Pasta _includes:

    Contém arquivos que podem ser incluídos em outros arquivos usando a sintaxe Liquid.

    Pasta _layouts:

    Contém templates que definem a estrutura de suas páginas. Você pode usar esses layouts para criar páginas consistentes.

    Pasta _posts:

    Contém os posts do blog, geralmente escritos em Markdown. Cada post é compilado em uma página HTML.

    Pasta _data:

    Contém dados estáticos que podem ser usados em seus templates, como configurações de menu ou informações de contato.

    Pasta _sass:

    Contém arquivos de estilo CSS pré-processados (Sass) que são compilados em CSS.

    Pasta _site:

    Esta pasta é gerada automaticamente pelo Jekyll quando você compila seu site. Ela contém todos os arquivos HTML, CSS e JavaScript que compõem seu site estático.

    Processo de Compilação

    Editar Arquivos:

    Faça suas alterações nos arquivos Markdown, HTML, Sass, etc.

    Compilar o Site:

    Execute o comando jekyll build no terminal para compilar seus arquivos e gerar a pasta _site.

    Servir o Site Localmente:

    Execute o comando jekyll serve para iniciar um servidor local e visualizar seu site em http://localhost:4000.

    Enviar para o GitHub Pages:

    Envie seu repositório para o GitHub e seu site será hospedado automaticamente em https://seuusuario.github.io/seu-repositorio.

    Exemplo de Estrutura de Arquivos:

        seu-repositorio/
        ├── _config.yml
        ├── _includes/
        ├── _layouts/
        ├── _posts/
        ├── _data/
        ├── _sass/
        ├── _site/
        ├── index.html
        └── about.md

    No Jekyll, a pasta _posts é usada principalmente para armazenar postagens de blog, que geralmente são arquivos Markdown (.md) ou HTML (.html) com um cabeçalho YAML. Esses arquivos são automaticamente processados e listados em páginas de índice de blog ou arquivos.

    Organização de Arquivos no Jekyll

    Aqui estão algumas práticas comuns para organizar diferentes tipos de conteúdo no Jekyll:

    Pasta _posts:

    Coloque arquivos de postagens de blog aqui, como 2024-12-15-nome-do-post.md. Cada arquivo de postagem deve começar com um cabeçalho YAML.

        ---
        layout: post
        title: "Meu Post"
        date: 2024-12-15 10:00:00 +0000
        categories: categoria1 categoria2
        ---
        Conteúdo do post aqui...

    Páginas de Conteúdo:

    Para arquivos .html ou .md que não são postagens de blog, você pode colocá-los na raiz do repositório ou em outras pastas personalizadas. Por exemplo, about.html ou projetos/index.md.

    Incluindo Arquivos no index.html:

    Para incluir arquivos específicos no index.html, você pode usar o Liquid, a linguagem de template do Jekyll. Por exemplo, para incluir todos os posts em uma página index.html, você pode usar:

    exemplo.html
    ---
    layout: default
    ---

    <h1>Posts Recentes</h1>
    <ul>
    {% for post in site.posts %}
    <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
        <p>{{ post.excerpt }}</p>
    </li>
    {% endfor %}
    </ul>

    Incluindo Conteúdo com _includes:

    Use a pasta _includes para fragmentos de código que você deseja incluir em várias páginas. Por exemplo, crie _includes/header.html e inclua-o em outras páginas com {% include header.html %}.

    Exemplo de Organização

        seu-repositorio/
        ├── _config.yml
        ├── _includes/
        │   └── header.html
        ├── _layouts/
        │   └── default.html
        ├── _posts/
        │   └── 2024-12-15-nome-do-post.md
        ├── about.html
        ├── index.html
        └── projetos/
            └── index.md
</details>    