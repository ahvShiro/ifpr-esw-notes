**Matéria:** [[OOP]]
**Tópicos:** #

**Problema 1: Gerenciador de Tarefas**  
Você está desenvolvendo um aplicativo de tarefas para ajudar usuários a organizarem suas atividades diárias. Cada tarefa deve ter um título, uma descrição, uma data de vencimento e uma prioridade. Os usuários poderão marcar tarefas como concluídas ou excluí-las quando não forem mais necessárias. O sistema deve permitir visualizar, adicionar, remover e atualizar tarefas de forma simples.

```mermaid
classDiagram
    class Tarefa
    Tarefa : Int id
    Tarefa : Int idUsuario
    Tarefa : String titulo
    Tarefa : String descricao
    Tarefa : Date dataVencimento
    Tarefa : Integer prioridade
    Tarefa : Bool status
    Tarefa : Date criadoEm
    Tarefa : Date atualizadoEm
    Tarefa : 
    
    class Usuario
    Usuario : Int id
    Usuario : String nome
    Usuario : String email
    Usuario : String senha
    Usuario : 
    Usuario :
    Usuario :
    Usuario :
    Usuario :
    
```

