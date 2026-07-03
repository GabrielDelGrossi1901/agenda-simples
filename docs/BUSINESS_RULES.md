# Regras de Negócio

Este documento descreve as regras de negócio iniciais do Agenda Simples.

## Regras de Agendamento

### RN001 - Agendamento deve estar vinculado a uma empresa

Todo agendamento deve pertencer a uma empresa prestadora de serviço.

### RN002 - Agendamento deve possuir cliente

Todo agendamento deve possuir um cliente responsável pelo horário reservado.

### RN003 - Agendamento deve possuir serviço

Todo agendamento deve estar associado a um serviço oferecido pela empresa.

### RN004 - Agendamento deve possuir profissional

Todo agendamento deve estar associado a um profissional responsável pela execução do serviço.

### RN005 - Profissional não pode ter conflito de horário

Um profissional não pode possuir dois agendamentos ativos no mesmo intervalo de horário.

### RN006 - Serviço deve possuir duração estimada

Todo serviço deve possuir uma duração estimada para permitir o cálculo do horário final do agendamento.

### RN007 - Agendamento deve respeitar a disponibilidade do profissional

Um agendamento só pode ser criado dentro dos horários de disponibilidade do profissional.

### RN008 - Profissional só pode executar serviços habilitados

Um profissional só pode ser agendado para serviços que ele está habilitado a realizar.

### RN009 - Cliente será vinculado a uma empresa

No MVP, o cliente será tratado como um cliente da empresa em que realizou o agendamento.

### RN010 - Agendamento será confirmado automaticamente

No MVP, quando um horário estiver disponível, o agendamento será criado com status Agendado.

## Status do Agendamento

Inicialmente, um agendamento poderá possuir os seguintes status:

- Agendado
- Cancelado
- Concluído

## Decisões para versões futuras

- Permitir cliente global na plataforma.
- Permitir preço diferente por profissional.
- Permitir reagendamento completo.
- Permitir confirmação manual de agendamento.
- Permitir bloqueios de agenda, férias e exceções.
- Permitir notificações por e-mail ou WhatsApp.