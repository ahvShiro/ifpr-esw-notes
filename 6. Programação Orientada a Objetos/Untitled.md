**Matéria:** [[OOP]]
**Tópicos:** #

**Problema 1: Gerenciador de Tarefas**  
Você está desenvolvendo um aplicativo de tarefas para ajudar usuários a organizarem suas atividades diárias. Cada tarefa deve ter um título, uma descrição, uma data de vencimento e uma prioridade. Os usuários poderão marcar tarefas como concluídas ou excluí-las quando não forem mais necessárias. O sistema deve permitir visualizar, adicionar, remover e atualizar tarefas de forma simples.

```mermaid
classDiagram
    class Tarefa
    Tarefa : String titulo
    Tarefa : String descricao
    Tarefa : Integer prioridade
    Tarefa : Date dataVencimento
    Tarefa : Bool status
    Tarefa : Date criadoEm
    Tarefa : Date atualizadoEm
    Tarefa : Usuario usuario
    
    class Usuario
    Usuario : String nome
    Usuario : String email
    Usuario : String senha
    
```

**Problema 2: Sistema de Votação Online**  
Uma escola quer criar um sistema online para eleger o representante de turma. Cada aluno poderá votar uma única vez em um dos candidatos. O sistema deve registrar os votos, garantir que ninguém vote duas vezes e exibir o vencedor ao final da votação. A proposta é criar uma aplicação simples e segura para conduzir eleições escolares.

```mermaid
classDiagram
    class Aluno
    Aluno : String nome
    Aluno : String registroDeAluno
    Aluno : Candidato alunoVotado
    
    Aluno <|-- Candidato : extends
    
    class Candidato
    Candidato : Int votos
    Candidato : Date dataInscricao
    
```

**Problema 3: Simulador de Corrida de Carros**  
Um jogo de corrida está sendo desenvolvido e precisa simular o comportamento de diferentes carros durante uma prova. Cada carro tem um modelo e uma velocidade máxima. Durante a corrida, os carros devem ser capazes de acelerar, frear e mostrar seu status atual (como a velocidade no momento). O sistema deve representar essas ações de forma que os comportamentos possam ser testados e comparados.

```mermaid
classDiagram
    class Carro
    Carro : String modelo
    Carro : String cor
    Carro : Double velocidadeMaxima
    Carro : Double velocidade
    Carro : Date ano
    Carro : Marca marca
	class Marca
	Marca : String nome
```
