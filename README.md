# Board de Tarefas em Java

Este projeto é uma aplicação simples de **Board de Tarefas** desenvolvida em **Java**, que permite a criação e gerenciamento de boards com regras específicas para a movimentação de cards. O sistema organiza as tarefas em colunas, seguindo regras pré-definidas de movimentação e bloqueio.

## Funcionalidades

- **Criação de Boards**: Permite criar boards com nome e colunas.
- **Colunas obrigatórias**:
  - **Inicial**: Onde os cards começam.
  - **Concluído**: Para tarefas finalizadas.
  - **Cancelado**: Para tarefas descartadas.
- **Colunas adicionais**: Você pode adicionar colunas do tipo **Pendente** livremente.
- **Movimentação de Cards**: Cards podem ser movidos entre colunas com base em regras específicas.
- **Status de Cards**: Os cards podem ser **bloqueados** ou **desbloqueados**, com requisitos de motivo para bloqueio/desbloqueio.

## Regras dos Boards

Cada board deve ter:

- **Nome**: Identificação única do board.
- **Colunas obrigatórias**:
  - **Inicial**: Onde os cards começam.
  - **Concluído**: Para tarefas finalizadas.
  - **Cancelado**: Para tarefas descartadas.
- **Colunas adicionais**: Podem ser adicionadas colunas do tipo **Pendente**.

Cada coluna possui:

- **Nome**: O título da coluna.
- **Ordem de exibição**: A posição da coluna no board.
- **Tipo**: Pode ser **Inicial**, **Pendente**, **Final** ou **Cancelamento**.

### Regras de disposição das colunas:

- **Somente uma coluna** de cada tipo especial (Inicial, Final, Cancelamento) pode existir.
- A **ordem das colunas** deve ser:
  - Inicial → Pendentes → Final → Cancelamento.

## Regras dos Cards

Cada card inclui:

- **Título**: Identificação da tarefa.
- **Descrição**: Detalhes adicionais sobre a tarefa.
- **Data de criação**: Data em que o card foi criado.
- **Status**: **Bloqueado** ou **Desbloqueado** .

### Movimentação dos Cards:

- Os cards **seguem a ordem das colunas** e **não podem pular etapas**.
- Cards podem ser **movidos diretamente para a coluna Cancelamento**, exceto se estiverem na coluna **Final**.

### Cards Bloqueados:

- **Cards bloqueados** não podem ser movidos entre as colunas.
- Para **bloquear ou desbloquear** um card, é necessário **informar um motivo**.
