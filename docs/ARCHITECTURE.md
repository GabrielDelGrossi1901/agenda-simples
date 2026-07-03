# Arquitetura do Projeto

## Visão Geral

O Agenda Simples será desenvolvido inicialmente como um monólito modular utilizando uma Clean Architecture simplificada.

O objetivo é organizar o código de forma clara, separando responsabilidades entre API, aplicação, domínio e infraestrutura.

Essa abordagem permite desenvolver um projeto simples o suficiente para aprendizado, mas estruturado o bastante para demonstrar boas práticas de Engenharia de Software.

## Estrutura Planejada

```text
src/
├── AgendaSimples.Api
├── AgendaSimples.Application
├── AgendaSimples.Domain
└── AgendaSimples.Infrastructure

tests/
├── AgendaSimples.UnitTests
└── AgendaSimples.IntegrationTests