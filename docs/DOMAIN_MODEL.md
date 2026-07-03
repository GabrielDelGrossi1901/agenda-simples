# Modelo de Domínio

## Objetivo

Este documento descreve as principais entidades do domínio do Agenda Simples e seus relacionamentos iniciais.

O objetivo é manter uma visão clara do negócio antes da implementação do código.

## Entidades Iniciais

### Empresa

Representa o negócio que oferece serviços aos clientes.

Exemplos:

- Barbearia
- Clínica
- Salão de beleza
- Consultório
- Pet shop
- Profissional autônomo

### Serviço

Representa um tipo de serviço oferecido pela empresa.

Exemplos:

- Corte de cabelo
- Barba
- Consulta
- Banho e tosa
- Manicure

Um serviço pode possuir informações como nome, descrição, duração estimada e preço.

### Profissional

Representa uma pessoa vinculada à empresa que pode realizar um ou mais serviços.

Um profissional pode ter uma agenda própria e estar disponível em determinados dias e horários.

### Cliente

Representa a pessoa que agenda e consome os serviços oferecidos pela empresa.

Um cliente pode realizar um ou mais agendamentos.

### Agendamento

Representa a reserva de um horário para que um cliente receba um serviço de uma empresa, realizado por um profissional específico.

Um agendamento deve conter informações como data, horário, serviço, cliente, profissional, empresa e status.

## Relacionamentos Iniciais

- Uma Empresa pode oferecer muitos Serviços.
- Uma Empresa pode possuir muitos Profissionais.
- Um Cliente pode possuir muitos Agendamentos.
- Um Profissional pode possuir muitos Agendamentos.
- Um Serviço pode estar presente em muitos Agendamentos.
- Um Agendamento pertence a uma Empresa.
- Um Agendamento pertence a um Cliente.
- Um Agendamento pertence a um Serviço.
- Um Agendamento pertence a um Profissional.

## Regras de Negócio Iniciais

- Um agendamento deve estar vinculado a uma empresa.
- Um agendamento deve possuir um cliente.
- Um agendamento deve possuir um serviço.
- Um agendamento deve possuir um profissional.
- Um agendamento deve possuir data e horário.
- Um profissional só deve ser agendado para serviços que ele pode realizar.
- Um profissional não deve possuir dois agendamentos no mesmo horário.
- Um serviço deve possuir uma duração estimada.

## Decisões Iniciais

- No MVP, o cliente será vinculado a uma empresa.
- A disponibilidade dos profissionais será definida por horários de trabalho.
- O preço pertence ao serviço, não ao profissional.
- Cancelamentos serão tratados por status.
- Reagendamentos serão tratados em versão futura.
- Agendamentos serão confirmados automaticamente quando o horário estiver disponível.

## Pontos para Evolução Futura

- Cliente global na plataforma.
- Preço de serviço por profissional.
- Reagendamento completo.
- Confirmação manual de agendamento.
- Bloqueios de agenda, férias e feriados.
- Notificações por e-mail ou WhatsApp.