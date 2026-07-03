# Mapa de Entidades e Atributos

Este documento descreve as entidades iniciais do Agenda Simples e seus atributos mínimos para o MVP.

O objetivo é mapear os dados necessários antes da implementação das classes de domínio.

## Observação sobre Multi-Tenant

Como o Agenda Simples será uma plataforma SaaS, a entidade Empresa representa o "tenant" do sistema.

No MVP, as principais entidades serão vinculadas a uma Empresa por meio de EmpresaId.

Isso permite que diferentes empresas utilizem a mesma plataforma mantendo seus dados separados.

## Entidades Principais

### Empresa

Representa o negócio que oferece serviços aos clientes.

Atributos iniciais:

- Id
- Nome
- Documento
- Email
- Telefone
- Ativo
- CriadoEm
- AtualizadoEm

### Serviço

Representa um tipo de serviço oferecido por uma empresa.

Atributos iniciais:

- Id
- EmpresaId
- Nome
- Descricao
- DuracaoEmMinutos
- Preco
- Ativo
- CriadoEm
- AtualizadoEm

### Profissional

Representa uma pessoa vinculada a uma empresa que pode realizar serviços.

Atributos iniciais:

- Id
- EmpresaId
- Nome
- Email
- Telefone
- Ativo
- CriadoEm
- AtualizadoEm

### Cliente

Representa uma pessoa que agenda e consome serviços oferecidos por uma empresa.

No MVP, o cliente será vinculado a uma empresa.

Atributos iniciais:

- Id
- EmpresaId
- Nome
- Email
- Telefone
- Ativo
- CriadoEm
- AtualizadoEm

### Agendamento

Representa a reserva de um horário para que um cliente receba um serviço de uma empresa, realizado por um profissional específico.

Atributos iniciais:

- Id
- EmpresaId
- ClienteId
- ProfissionalId
- ServicoId
- DataHoraInicio
- DataHoraFim
- Status
- Observacao
- CriadoEm
- AtualizadoEm

## Entidades de Apoio

### ProfissionalServico

Representa quais serviços um profissional está habilitado a realizar.

Essa entidade é necessária porque um profissional pode realizar vários serviços e um serviço pode ser realizado por vários profissionais.

Atributos iniciais:

- ProfissionalId
- ServicoId

### DisponibilidadeProfissional

Representa os horários em que um profissional está disponível para receber agendamentos.

Atributos iniciais:

- Id
- ProfissionalId
- DiaDaSemana
- HoraInicio
- HoraFim
- Ativo

## Enumerações

### StatusAgendamento

Representa o estado atual de um agendamento.

Valores iniciais:

- Agendado
- Cancelado
- Concluido

## Regras Representadas no Modelo

- EmpresaId permite separar os dados de cada empresa dentro da plataforma.
- Servico possui DuracaoEmMinutos para permitir calcular o horário final do agendamento.
- Agendamento possui DataHoraInicio e DataHoraFim para permitir validação de conflito de horário.
- ProfissionalServico permite validar se um profissional pode executar determinado serviço.
- DisponibilidadeProfissional permite validar se o agendamento está dentro da agenda de trabalho do profissional.
- StatusAgendamento permite controlar agendamentos ativos, cancelados e concluídos.

## Pontos para Revisão Futura

- Avaliar se Documento será obrigatório para Empresa.
- Avaliar se Email será obrigatório para Cliente.
- Avaliar se o Cliente poderá se tornar global na plataforma.
- Avaliar se Serviço terá categorias.
- Avaliar se Profissional terá especialidades.
- Avaliar se disponibilidade precisará suportar pausas, férias e exceções.