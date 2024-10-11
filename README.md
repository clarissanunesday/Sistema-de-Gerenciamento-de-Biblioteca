# Sistema de Gerenciamento de Biblioteca

Este projeto implementa um sistema simples de gerenciamento de uma biblioteca, onde é possível registrar autores, livros, empréstimos e devoluções. O banco de dados foi projetado para armazenar informações sobre os autores, livros disponíveis e os empréstimos realizados pelos usuários.

## Funcionalidades

- **Cadastro de Autores**: Permite armazenar informações sobre os autores de livros, como nome e nacionalidade.
- **Cadastro de Livros**: Permite o registro de livros com detalhes sobre o título, ano de publicação, gênero e autor.
- **Gestão de Empréstimos**: Armazena informações sobre os empréstimos de livros realizados pelos usuários, incluindo a data de empréstimo e devolução.
- **Consultas**:
  - Listar todos os livros disponíveis com seus autores e ano de publicação.
  - Consultar empréstimos em aberto.
- **Atualização de Dados**: Atualizar a data de devolução de um empréstimo específico.
- **Exclusão de Dados**: Remover registros de empréstimos e livros do sistema.

## Estrutura do Projeto

1. **Autores**: Contém informações sobre os autores, como nome e nacionalidade.
2. **Livros**: Cada livro possui um título, autor, ano de publicação e gênero.
3. **Empréstimos**: Armazena dados sobre os empréstimos de livros, como a data de empréstimo, devolução e o nome do usuário.

## Estrutura do Banco de Dados

### Tabelas:

- **Autores**:
  - `AutorID`: Identificador único para o autor.
  - `Nome`: Nome do autor.
  - `Nacionalidade`: Nacionalidade do autor.

- **Livros**:
  - `LivroID`: Identificador único para o livro.
  - `Titulo`: Título do livro.
  - `AutorID`: Identificador do autor relacionado ao livro.
  - `AnoPublicacao`: Ano de publicação do livro.
  - `Genero`: Gênero literário do livro.

- **Empréstimos**:
  - `EmprestimoID`: Identificador único para o empréstimo.
  - `LivroID`: Identificador do livro emprestado.
  - `DataEmprestimo`: Data do empréstimo.
  - `DataDevolucao`: Data de devolução (pode ser nula enquanto o livro não for devolvido).
  - `NomeUsuario`: Nome do usuário que fez o empréstimo.

## Consultas Disponíveis

1. **Listar todos os livros com seus autores**:
   - Lista os títulos dos livros disponíveis, seus autores e o ano de publicação.

2. **Listar empréstimos em aberto**:
   - Exibe todos os empréstimos que ainda não tiveram a devolução registrada.

## Como Usar

1. **Criar o Banco de Dados**:
   Execute o script SQL fornecido para criar o banco de dados e as tabelas necessárias.
   
2. **Inserir Dados**:
   Insira os dados de autores, livros e empréstimos utilizando os scripts SQL fornecidos.

3. **Consultas**:
   Use os comandos SQL para realizar consultas e manipular os dados conforme necessário.

4. **Atualizações**:
   Atualize a data de devolução de um empréstimo ou remova registros de livros e seus empréstimos associados.

## Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

## Requisitos

- MySQL ou outro sistema de gerenciamento de banco de dados SQL compatível.
- Editor SQL para execução das consultas e scripts.
