# Trabalho de Metodologias Ágeis — 2º Ano CT

**Alunos:** Ygor Gustavo Gonçalves Da Silva e Geovanna Luíza Duarte Costa  
**Turma:** 2º Ano CT  
**Professor:** Jason  
**Data:** 25/10/2026  

---

## O que é GitHub?

GitHub é uma plataforma online para hospedar projetos e colaborar neles. Pessoas e equipes podem guardar arquivos, acompanhar alterações e conversar sobre melhorias. É muito usado no desenvolvimento de software, mas também pode organizar documentos, materiais de estudo e outros arquivos.

O GitHub utiliza o Git, um sistema de controle de versão. Em termos simples, o Git registra mudanças ao longo do tempo. Assim, é possível consultar versões anteriores e entender o que foi alterado. O GitHub oferece uma interface e ferramentas de colaboração em torno desses repositórios.

### Conceitos importantes

* **Repositório (repository):** espaço de um projeto que reúne arquivos e histórico de alterações. Pode ser público ou privado.
* **Commit:** registro de uma alteração, acompanhado de uma mensagem que explica o que foi feito.
* **Branch (ramificação):** linha de trabalho separada, útil para experimentar mudanças sem alterar imediatamente a versão principal.
* **Pull request:** proposta para revisar e integrar mudanças de uma branch em outra. Permite discutir as alterações antes de incorporá-las.
* **README:** arquivo de apresentação do projeto. Normalmente explica seu objetivo e como utilizá-lo. O GitHub costuma exibi-lo na página inicial do repositório.

---

## A Ligação do GitHub com a Aula 2 da Semana 21: Pipeline de Feedback e Cultura DevOps

Na nossa disciplina, aprendemos sobre a **Cultura DevOps**, que busca unir quem desenvolve o sistema (Dev) e quem cuida da infraestrutura/operação (Ops) para entregar software com mais agilidade e qualidade[cite: 2].

O tema central da **Aula 2 (SISANO1C3B4S21A2)** é o **Pipeline de Feedback**[cite: 2]. Em termos simples, um pipeline de feedback é uma esteira automática que pega o código alterado, faz o *build* (compilação), executa os testes e devolve uma resposta rápida à equipe sobre o estado daquele código[cite: 7, 8].

### O Custo do Atraso e a Mentalidade *Fail Fast*
A regra de ouro que vimos na aula é: **quanto mais tempo demoramos para descobrir um erro, mais caro e complexo fica corrigi-lo**[cite: 9]. 
* Se um bug for descoberto em 2 minutos logo que o código é enviado, o aluno/desenvolvedor corrige-o na hora[cite: 6].
* Se o bug for para produção e ficar falhando durante o fim de semana, o prejuízo e o retrabalho são enormes[cite: 6].

Por isso usamos a mentalidade ***fail fast*** (falhar rápido)[cite: 7, 12]: queremos que o sistema aponte qualquer erro o mais cedo possível. Trabalhar em **pequenos lotes** (fazer alterações pequenas e frequentes em vez de um código gigante de uma só vez) ajuda a equipe a receber feedback quase instantâneo[cite: 9].

---

## Como os Recursos do GitHub Sustentam o Ciclo de Feedback

O GitHub não é só uma pasta na nuvem. Tem ferramentas que garantem tanto o **feedback humano** como o **feedback automatizado**[cite: 1, 2]:

### A. Issues (Feedback de Problemas e Ideias)
As **Issues** funcionam como um painel de recados e tarefas do projeto[cite: 8]. É onde qualquer membro da equipe ou usuário registra um bug encontrado, sugere uma melhoria ou detalha uma nova tarefa. O feedback começa aqui, mapeando a necessidade antes de o código ser escrito.

### B. Pull Requests (Feedback Humano e Revisão por Pares)
Quando vamos enviar uma alteração para o projeto principal, criamos um **Pull Request (PR)**. O PR é a etapa de feedback humano: os colegas de equipe analisam o código, fazem comentários, sugerem mudanças na lógica e só aprovam quando tudo estiver correto. Isso evita que códigos com erros entrem diretamente na versão principal.

### C. GitHub Actions (Feedback Automatizado — Integração Contínua)
O **GitHub Actions** é a ferramenta que constrói o pipeline de feedback propriamente dito[cite: 8]. Sempre que alguém faz um commit ou abre um Pull Request, o GitHub Actions dispara
