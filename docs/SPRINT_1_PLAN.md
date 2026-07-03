# Sprint 1 - Base Técnica e Primeira Entidade

## Objetivo da Sprint

Criar a estrutura técnica inicial do projeto Agenda Simples utilizando .NET, ASP.NET Core e uma arquitetura em camadas.

Nesta sprint, o foco será criar a base do projeto e implementar a primeira entidade do domínio: Empresa.

## Escopo da Sprint

### 1. Estrutura da Solution

- Criar a solution .NET do projeto.
- Criar os projetos principais:
  - AgendaSimples.Api
  - AgendaSimples.Application
  - AgendaSimples.Domain
  - AgendaSimples.Infrastructure
- Criar projeto de testes:
  - AgendaSimples.UnitTests

### 2. Configuração Inicial da API

- Configurar projeto Web API.
- Configurar Swagger.
- Criar endpoint de Health Check.
- Validar se a API executa localmente.

### 3. Primeira Entidade do Domínio

- Criar entidade Empresa.
- Definir atributos iniciais:
  - Id
  - Nome
  - Documento
  - Email
  - Telefone
  - Ativo
  - CriadoEm
  - AtualizadoEm

### 4. Regras Iniciais da Entidade Empresa

- Empresa deve possuir nome.
- Empresa deve possuir e-mail.
- Empresa deve iniciar como ativa.
- Empresa deve possuir data de criação.

### 5. Testes Unitários

- Criar testes unitários para validar a criação de uma Empresa.
- Criar testes para regras básicas da entidade.

### 6. Documentação

- Atualizar PROJECT_CONTEXT.md ao final da sprint.
- Atualizar LEARNING_LOG.md com aprendizados.
- Registrar decisões relevantes em DECISIONS.md.

## Fora do Escopo da Sprint

Nesta sprint, NÃO serão implementados:

- Banco de dados
- Entity Framework Core
- Autenticação
- Login
- JWT
- Serviço
- Profissional
- Cliente
- Agendamento
- Docker
- AWS

Esses itens serão tratados em sprints futuras.

## Definition of Done

A Sprint 1 será considerada concluída quando:

- A solution .NET estiver criada.
- A API estiver executando localmente.
- O Swagger estiver funcionando.
- O Health Check estiver disponível.
- A entidade Empresa estiver criada na camada Domain.
- Existirem testes unitários básicos para Empresa.
- A documentação estiver atualizada.
- O código estiver versionado no GitHub.