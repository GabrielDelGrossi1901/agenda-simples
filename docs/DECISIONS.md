# Decisões do Projeto

Este arquivo registra decisões técnicas e de produto tomadas durante o desenvolvimento.

## 2026-07-03 - Início do projeto

### Decisão

Criar o projeto Agenda Simples como uma plataforma SaaS de agendamento de serviços.

### Motivo

O domínio de agendamento permite estudar problemas reais de produto e engenharia, como gestão de horários, conflitos de agenda, serviços, profissionais, clientes, autenticação, banco de dados, testes e escalabilidade.

### Alternativas consideradas

- Sistema de gestão de ativos de TI
- Sistema específico para barbearias

### Justificativa

A escolha por uma plataforma genérica de agendamento permite maior flexibilidade de modelagem e demonstra melhor capacidade de pensar em soluções extensíveis.

## 2026-07-03 - Definição da arquitetura inicial

### Decisão

Utilizar um monólito modular com Clean Architecture simplificada.

### Motivo

O projeto tem como objetivo servir como projeto vitrine e ambiente de aprendizado em Engenharia de Software. Uma arquitetura em camadas permite estudar separação de responsabilidades, regras de negócio, testes, persistência e APIs REST sem adicionar complexidade desnecessária no início.

### Alternativas consideradas

- Arquitetura simples com apenas uma API
- Microservices
- Arquitetura baseada em camadas tradicionais
- Clean Architecture completa

### Justificativa

Microservices foram descartados por adicionarem complexidade operacional desnecessária para o momento atual do projeto. Uma API simples demais também foi descartada por não demonstrar bem conceitos de engenharia. A Clean Architecture simplificada foi escolhida por equilibrar aprendizado, organização e aplicabilidade prática.

## 2026-07-03 - Definição de multi-tenancy simples

### Decisão

Utilizar a entidade Empresa como unidade principal de separação de dados do sistema.

### Motivo

Como o Agenda Simples será uma plataforma SaaS, diferentes empresas poderão utilizar a mesma aplicação. Por isso, entidades como Serviço, Profissional, Cliente e Agendamento serão vinculadas a uma Empresa.

### Justificativa

Essa abordagem permite iniciar o projeto com uma estratégia simples de multi-tenancy, utilizando EmpresaId nas entidades principais. Isso evita complexidade prematura, mas mantém o modelo preparado para atender múltiplas empresas.