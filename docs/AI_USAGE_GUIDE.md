# Guia de Uso da IA no Projeto

Este documento define como a Inteligência Artificial será utilizada durante o desenvolvimento do Agenda Simples.

## Objetivo

A IA será utilizada como apoio ao aprendizado, revisão técnica, discussão de arquitetura e melhoria de código.

A IA não será utilizada como programador principal do projeto.

## Papéis da IA

Durante o projeto, a IA poderá atuar como:

- Mentor técnico
- Revisor de código
- Apoio em arquitetura
- Apoio em estudos
- Simulador de entrevistas técnicas

## Regras de Uso

### Regra 1 - O desenvolvedor deve tentar primeiro

Antes de pedir uma solução completa, o desenvolvedor deve tentar entender o problema e propor uma abordagem inicial.

### Regra 2 - A IA não deve entregar código pronto imediatamente

Sempre que possível, a IA deve explicar conceitos, fazer perguntas e revisar ideias antes de sugerir implementação.

### Regra 3 - Toda decisão importante deve ser documentada

Decisões relevantes devem ser registradas em `DECISIONS.md`.

### Regra 4 - O contexto do projeto deve ser mantido nos arquivos

O histórico do chat não deve ser a fonte principal de memória do projeto.

A fonte principal de contexto será a documentação dentro da pasta `docs`.

### Regra 5 - Chats temporários devem receber contexto

Ao abrir um novo chat para uma tarefa específica, o desenvolvedor deve fornecer o conteúdo atualizado de `PROJECT_CONTEXT.md`.

### Regra 6 - A IA deve ajudar no aprendizado

A IA deve explicar o motivo das decisões técnicas e não apenas fornecer respostas prontas.

### Regra 7 - O código deve ser compreendido antes de ser aceito

Nenhum código sugerido pela IA deve ser utilizado sem que o desenvolvedor compreenda sua finalidade.

## Forma Recomendada de Pedir Ajuda

Antes de pedir ajuda, informar:

- O que estou tentando fazer
- O que já tentei
- Qual é minha dúvida
- Qual comportamento esperado
- Qual erro ocorreu, se houver

## Exemplo de boa pergunta

"Estou tentando criar a entidade Empresa no domínio. Minha ideia é validar Nome e Email no construtor. Pensei em lançar exceção quando esses campos estiverem vazios. Essa abordagem faz sentido para uma entidade de domínio?"

## Exemplo de pergunta ruim

"Cria a entidade Empresa para mim."