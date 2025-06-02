# Sistema Gerenciamento de Biblioteca

Este é um sistema de gerenciamento de biblioteca desenvolvido em Python com SQLite como banco de dados.

## 📚 Funcionalidades

- ### Cadastro de Livros

    - Adicionar novos livros ao acervo
    - Informar título, autor, ano de publicação e quantidade de cópias
    - Controle automático de cópias disponíveis

- ### Cadastro de Usuários

    - Registrar novos usuários da biblioteca
    - Armazenar nome, identificação única e contato

- ### Empréstimos

    - Realizar empréstimos de livros
    - Prazo padrão de 14 dias para devolução
    - Controle automático de disponibilidade

- ### Devoluções

    - Registrar devolução de livros
    - Atualizar status de disponibilidade
    - Identificar devoluções com atraso

- ### Consultas

    - Buscar livros por título, autor ou ano
    - Verificar disponibilidade
    - Listar todos os livros cadastrados

- ### Relatórios

  - Livros disponíveis
  - Livros emprestados
  - Usuários cadastrados
  - Empréstimos ativos
  - Histórico de empréstimos (com status de atraso)

## 🛠️ Tecnologias Utilizadas

- Python 3
  
- SQLite (banco de dados embutido)
  
- Biblioteca sqlite3 para acesso ao banco de dados
  
- Biblioteca datetime para controle de prazos

## ⚙️ Instalação e Execução

1. Certifique-se de ter Python 3 instalado em seu sistema

2. Clone ou faça o download deste repositório

3. Execute o arquivo principal:

       python biblioteca.py

O sistema criará automaticamente o banco de dados biblioteca.db na primeira execução.

## 📊 Estrutura do Banco de Dados

O sistema utiliza 3 tabelas principais:

1. livros
    - id: Chave primária
    - titulo: Título do livro
    - autor: Autor do livro
    - ano_publicacao: Ano de publicação
    - copias_disponiveis: Quantidade de cópias disponíveis
    - copias_totais: Quantidade total de cópias

2. usuarios
    - id: Chave primária
    - nome: Nome completo do usuário
    - identificacao: Número de identificação único
    - contato: Informações de contato (telefone/email)

3. emprestimos
    - id: Chave primária
    - livro_id: Chave estrangeira para livros
    - usuario_id: Chave estrangeira para usuários
    - data_emprestimo: Data do empréstimo
    - data_devolucao_prevista: Data prevista para devolução
    - data_devolucao_real: Data real de devolução (NULL se não devolvido)

## 📝 Licença

Este projeto está licenciado sob a licença MIT. Consulte o arquivo LICENSE para obter mais informações.
