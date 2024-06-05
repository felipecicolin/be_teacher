# BeTeacher - Backend

Este repositório contém o backend do projeto **BeTeacher**, desenvolvido utilizando Ruby on Rails com o banco de dados PostgreSQL. O objetivo deste projeto é fornecer uma plataforma para facilitar a interação entre tutores e alunos. O frontend deste projeto é um aplicativo móvel desenvolvido em Flutter/Dart.

## Tecnologias Utilizadas

- **Backend**: Ruby on Rails 7.x
- **Banco de Dados**: PostgreSQL 13.x
- **Autenticação**: Devise
- **Testes**: RSpec
- **Frontend**: Flutter/Dart

## Funcionalidades

- Cadastro e autenticação de usuários (tutores e alunos)
- Criação e gerenciamento de perfis de tutores
- Listagem e busca de tutores
- Agendamento de sessões de tutoria
- Sistema de avaliações e feedbacks

## Configuração do Ambiente de Desenvolvimento

### Pré-requisitos

Certifique-se de ter os seguintes itens instalados:

- Ruby (versão 3.0.0 ou superior)
- Rails (versão 7.0.0 ou superior)
- PostgreSQL (versão 13.0 ou superior)
- Node.js
- Yarn

### Passos para configuração

1. Clone o repositório:

   ```bash
   git clone https://github.com/rafavanzo/be_teacher.git
   cd be_teacher
   ```

2. Instale as dependências:

   ```bash
   bundle install
   yarn install
   ```

3. Configure o banco de dados:

   Crie um arquivo `config/database.yml` com as configurações do seu banco de dados PostgreSQL. Você pode usar o exemplo `config/database.yml.example` como base.

   ```yml
   default: &default
     adapter: postgresql
     encoding: unicode
     pool: 5
     username: seu-usuario
     password: sua-senha
     host: localhost

   development:
     <<: *default
     database: be_teacher_development

   test:
     <<: *default
     database: be_teacher_test

   production:
     <<: *default
     database: be_teacher_production
     username: nome_de_usuario_de_producao
     password: senha_de_producao
   ```

4. Crie e migre o banco de dados:

   ```bash
   rails db:create
   rails db:migrate
   ```

5. Popule o banco de dados com dados iniciais (opcional):

   ```bash
   rails db:seed
   ```

6. Inicie o servidor:

   ```bash
   rails server
   ```

   O servidor estará disponível em `http://localhost:3000`.

## Testes

Para rodar a suíte de testes, utilize o comando:

```bash
rspec
```

## Contribuição

Contribuições são bem-vindas! Por favor, siga os passos abaixo:

1. Faça um fork do projeto.
2. Crie uma branch para sua feature (`git checkout -b feature/nome-da-feature`).
3. Commite suas mudanças (`git commit -am 'Adicionei uma nova feature'`).
4. Faça o push para a branch (`git push origin feature/nome-da-feature`).
5. Abra um Pull Request.

## Licença

Este projeto está licenciado sob a MIT License. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## Contato

Para mais informações ou dúvidas, entre em contato com [rafavanzo@gmail.com](mailto:rafavanzo@gmail.com).

---

Esperamos que este projeto seja útil para você. Bons estudos e boa tutoria!