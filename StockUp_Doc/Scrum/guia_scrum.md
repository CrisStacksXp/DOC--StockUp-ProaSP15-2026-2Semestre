# Scrum — Guia rápido de estudos

> **Objetivo:** entender os fundamentos do Scrum, como ele funciona e como aplicá-lo em projetos de software.

## 1. O que é Scrum?

Scrum é um **framework ágil** usado para desenvolver, entregar e manter produtos complexos.

Ele organiza o trabalho em ciclos curtos chamados **Sprints**. Ao longo desses ciclos, a equipe cria partes funcionais do produto, recebe feedback e adapta o planejamento.

**Importante:** Scrum é um framework, não uma metodologia prescritiva. Ele define uma estrutura com responsabilidades, eventos, artefatos e regras, mas não determina todos os detalhes de como o trabalho deve ser feito.

## 2. Os fundamentos

O Scrum se baseia no **empirismo**: aprender com a experiência e tomar decisões a partir do que é observado.

Seus três pilares são:

| Pilar | Significado | Exemplo |
|---|---|---|
| **Transparência** | O trabalho e as informações importantes ficam visíveis. | Backlog atualizado e critérios claros. |
| **Inspeção** | O progresso e os resultados são avaliados com frequência. | Conferir se a funcionalidade atende aos requisitos. |
| **Adaptação** | O plano ou o processo é ajustado quando necessário. | Rever a abordagem após encontrar um problema. |

### Os cinco valores

- **Compromisso:** dedicar-se aos objetivos da equipe.
- **Foco:** concentrar-se no trabalho da Sprint.
- **Abertura:** compartilhar progresso, dificuldades e aprendizados.
- **Respeito:** reconhecer as pessoas e suas capacidades.
- **Coragem:** enfrentar problemas e tomar decisões difíceis.

## 3. Quem faz parte do Scrum Team?

O Scrum Team tem três responsabilidades:

| Responsabilidade | Principal função |
|---|---|
| **Product Owner (PO)** | Maximizar o valor do produto e ordenar o Product Backlog. |
| **Scrum Master (SM)** | Ajudar todos a compreender e aplicar o Scrum; melhorar a eficácia da equipe. |
| **Developers** | Criar o incremento e garantir sua qualidade. |

### Entenda cada papel

**Product Owner**
- Define e comunica o Product Goal.
- Cria e esclarece itens do Product Backlog.
- Ordena os itens conforme seu valor e importância.
- Garante que o Product Backlog seja transparente e compreensível.

**Scrum Master**
- Ensina e orienta sobre o Scrum.
- Ajuda a remover impedimentos.
- Facilita a melhoria contínua.
- Apoia a autogestão da equipe.

**Developers**
- Planejam como realizar o trabalho.
- Desenvolvem e testam o produto.
- Adaptam o plano diariamente.
- Entregam um incremento que atende à Definition of Done.

> **Para memorizar:** PO cuida do valor e da ordem do backlog; Scrum Master cuida da eficácia e do uso correto do Scrum; Developers constroem o incremento.

## 4. Os cinco eventos

A **Sprint** é o evento que contém os outros quatro. Cada Sprint tem duração fixa de **um mês ou menos**.

| Evento | Para que serve? | Duração máxima em uma Sprint de 1 mês |
|---|---|---:|
| **Sprint** | Ciclo de trabalho para produzir um incremento. | 1 mês |
| **Sprint Planning** | Planejar por que, o que e como trabalhar. | 8 horas |
| **Daily Scrum** | Inspecionar o progresso e adaptar o plano diário. | 15 minutos |
| **Sprint Review** | Avaliar o resultado com stakeholders e discutir próximos passos. | 4 horas |
| **Sprint Retrospective** | Identificar melhorias na forma de trabalhar. | 3 horas |

Para Sprints menores, os eventos normalmente são mais curtos.

### O que acontece em cada evento?

1. **Sprint Planning:** a equipe define a Sprint Goal, seleciona itens do Product Backlog e planeja como executá-los.
2. **Daily Scrum:** os Developers verificam o progresso em direção à Sprint Goal e ajustam o plano.
3. **Sprint Review:** equipe e stakeholders inspecionam o incremento e conversam sobre o que fazer em seguida.
4. **Sprint Retrospective:** o Scrum Team avalia como melhorar qualidade e eficácia na próxima Sprint.

**Atenção:** a Daily Scrum não é uma reunião de cobrança individual. É um momento de planejamento e alinhamento dos Developers.

## 5. Os três artefatos

Os artefatos representam o trabalho ou o valor produzido. Cada um possui um compromisso associado.

| Artefato | O que representa? | Compromisso |
|---|---|---|
| **Product Backlog** | Lista ordenada do que pode melhorar o produto. | Product Goal |
| **Sprint Backlog** | Sprint Goal, itens selecionados e plano de execução. | Sprint Goal |
| **Incremento** | Resultado utilizável produzido e integrado ao produto. | Definition of Done |

### Exemplos simples

**Product Backlog**
- Cadastro de usuários.
- Login.
- Recuperação de senha.
- Relatório de despesas.

**Sprint Backlog**
- Criar formulário de cadastro.
- Implementar validação.
- Conectar ao banco de dados.
- Testar o cadastro.

**Incremento**
- Funcionalidade de cadastro implementada, testada e integrada ao produto, atendendo à Definition of Done.

### Os três compromissos

- **Product Goal:** objetivo de longo prazo do produto.
- **Sprint Goal:** objetivo único da Sprint.
- **Definition of Done (DoD):** descrição formal das condições de qualidade que o incremento precisa cumprir para ser considerado concluído.

## 6. Como funciona o ciclo Scrum?

```text
Product Backlog
      |
      v
Sprint Planning
      |
      v
Sprint Backlog
      |
      v
+---------------------------+
|          SPRINT           |
|                           |
|  Desenvolvimento          |
|  Daily Scrum              |
|  Inspeção e adaptação     |
|                           |
+---------------------------+
      |
      v
Incremento
      |
      v
Sprint Review
      |
      v
Sprint Retrospective
      |
      v
Próxima Sprint
```

O ciclo se repete. O feedback e os aprendizados ajudam a equipe a decidir os próximos passos.

## 7. Exemplo prático: sistema financeiro

Imagine uma equipe desenvolvendo uma aplicação para registrar receitas e despesas.

**Product Goal:** criar uma aplicação que ajude usuários a acompanhar suas finanças pessoais.

| Sprint | Sprint Goal | Possível incremento |
|---|---|---|
| 1 | Permitir acesso à aplicação. | Cadastro e login funcionais. |
| 2 | Registrar movimentações. | Cadastro de receitas e despesas. |
| 3 | Visualizar a situação financeira. | Saldo e relatório simples. |

Ao final de cada Sprint, a equipe inspeciona o resultado, coleta feedback e adapta o Product Backlog quando necessário.

## 8. Scrum e ferramentas

Scrum não exige uma ferramenta específica. Algumas opções ajudam a visualizar e organizar o trabalho:

- **Trello:** quadros e cartões para acompanhar tarefas.
- **Jira:** planejamento e acompanhamento de projetos de software.
- **GitHub Projects:** organização de tarefas integrada aos repositórios.
- **Azure DevOps:** planejamento, desenvolvimento e entrega de software.
- **Notion:** documentação e organização de informações.

A ferramenta apoia o trabalho; ela não substitui os princípios e eventos do Scrum.

## 9. Vantagens e cuidados

**Vantagens**
- Entregas frequentes de valor.
- Maior transparência.
- Feedback recorrente.
- Adaptação a mudanças.
- Inspeção e melhoria contínuas.

**Cuidados**
- Exige colaboração e comunicação.
- Objetivos pouco claros prejudicam as Sprints.
- Mudanças constantes sem alinhamento podem gerar desorganização.
- Adotar reuniões e ferramentas sem compreender o framework não significa aplicar Scrum corretamente.

## 10. Resumo para memorizar

- **Scrum:** framework ágil para produtos complexos.
- **Empirismo:** decisões baseadas em experiência e observação.
- **3 pilares:** transparência, inspeção e adaptação.
- **5 valores:** compromisso, foco, abertura, respeito e coragem.
- **3 responsabilidades:** Product Owner, Scrum Master e Developers.
- **5 eventos:** Sprint, Sprint Planning, Daily Scrum, Sprint Review e Sprint Retrospective.
- **3 artefatos:** Product Backlog, Sprint Backlog e Incremento.
- **3 compromissos:** Product Goal, Sprint Goal e Definition of Done.

### Macete rápido

- **PO:** o que gera valor e qual a prioridade?
- **SM:** como ajudar a equipe a usar Scrum e melhorar?
- **Developers:** como construir o incremento?
- **Planning:** planejar.
- **Daily:** inspecionar o progresso e adaptar.
- **Review:** avaliar o produto.
- **Retrospective:** melhorar o processo.

## 11. Teste rápido

Tente responder sem consultar o material:

1. Quais são os três pilares do Scrum?
2. Qual é a responsabilidade principal do Product Owner?
3. Qual é a função do Scrum Master?
4. Quem cria o incremento?
5. Qual evento diário dura 15 minutos?
6. Qual é a diferença entre Sprint Review e Sprint Retrospective?
7. Qual artefato contém a lista ordenada de necessidades do produto?
8. O que é a Definition of Done?
9. Qual é a duração máxima de uma Sprint?
10. Scrum é uma metodologia ou um framework?

<details>
<summary>Ver respostas</summary>

1. Transparência, inspeção e adaptação.
2. Maximizar o valor do produto e gerenciar o Product Backlog.
3. Ajudar na compreensão e aplicação do Scrum e melhorar a eficácia do Scrum Team.
4. Os Developers.
5. Daily Scrum.
6. Review avalia o produto e seus resultados; Retrospective avalia como a equipe trabalha.
7. Product Backlog.
8. Descrição formal dos critérios de qualidade que o incremento deve cumprir.
9. Um mês ou menos.
10. Framework.

</details>

## 12. Referências para aprofundamento

1. SCHWABER, Ken; SUTHERLAND, Jeff. **O Guia do Scrum (2020)**. [Versão oficial em português brasileiro (PDF)](https://scrumguides.org/docs/scrumguide/v2020/2020-Scrum-Guide-PortugueseBR-3.0.pdf).
2. [Scrum Guides — Guia oficial](https://scrumguides.org/).
3. [Scrum.org — Recursos de aprendizagem](https://www.scrum.org/resources).

