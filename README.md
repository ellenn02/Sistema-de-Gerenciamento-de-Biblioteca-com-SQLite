# Sistema de Gerenciamento de Biblioteca com SQLite

## Descrição

Este projeto é um sistema simples de gerenciamento de uma biblioteca, desenvolvido em Python utilizando o banco de dados SQLite. Ele permite o gerenciamento de autores, livros e empréstimos de livros por diferentes usuários. O sistema é capaz de registrar autores, inserir livros no catálogo, controlar os empréstimos e exibir os registros do banco de dados.

## Funcionalidades

- **Gerenciamento de Autores**: Adicionar e listar autores da biblioteca.
- **Gerenciamento de Livros**: Inserir livros e associá-los aos autores, listar todos os livros do catálogo.
- **Controle de Empréstimos**: Registrar empréstimos de livros e monitorar devoluções.
  
## Estrutura do Banco de Dados

O banco de dados contém as seguintes tabelas:

- **Autores**
  - `AutorID`: Identificador único do autor.
  - `Nome`: Nome do autor.
  - `Nacionalidade`: Nacionalidade do autor.

- **Livros**
  - `LivroID`: Identificador único do livro.
  - `Titulo`: Título do livro.
  - `AutorID`: Referência ao autor do livro.
  - `AnoPublicacao`: Ano de publicação do livro.
  - `Genero`: Gênero do livro.

- **Empréstimos**
  - `EmprestimoID`: Identificador único do empréstimo.
  - `LivroID`: Referência ao livro emprestado.
  - `DataEmprestimo`: Data em que o livro foi emprestado.
  - `DataDevolucao`: Data em que o livro foi devolvido (ou `NULL` se não foi devolvido).
  - `NomeUsuario`: Nome do usuário que pegou o livro emprestado.

## Como Executar

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/nome-do-repositorio.git
   cd nome-do-repositorio
