# Trabalho de Metodologias Ágeis: O Papel do GitHub no Pipeline de Feedback DevOps

**Alunos:** Ygor Gustavo Gonçalves da Silva e Geovanna Luíza Duarte Costa  
**Turma:** 2º Ano CT  
**Professor:** Jason  
**Componente Curricular:** Desenvolvimento de Sistemas — Unidade 7 / Semana 21  
**Código da Aula de Referência:** SISANO1C3B4S21A2 (Aula 2: Pipeline de feedback)  
**Repositório Oficial:** https://github.com/gus0xz/Trabalho-de-Metodologias-ageis-2-Ano-CT  

---

## 1. O que é o GitHub, para que serve e como funciona?

Antes de falarmos de pipeline e automação, precisamos de entender a ferramenta principal que usamos no dia a dia do curso de Desenvolvimento de Sistemas: o **GitHub**[cite: 1, 2].

* **O que é e para que serve:** O GitHub é uma plataforma na nuvem para hospedar e gerir projetos de código-fonte usando o **Git**[cite: 1, 2]. Na prática, serve como o ponto de encontro da equipa de desenvolvimento. Em vez de estarmos a enviar pastas comprimidas ou ficheiros por mensagem, centralizamos todo o projeto no GitHub de forma organizada, segura e com histórico completo[cite: 1, 2].
* **Como funciona:** Enquanto o Git controla as alterações no nosso computador local (através dos *commits*), o GitHub leva tudo isso para a nuvem e adiciona recursos de colaboração[cite: 1, 2]. Permite que vários alunos ou programadores trabalhem na mesma aplicação ao mesmo tempo, criando ramificações (*branches*), sem o risco de um apagar o código do outro[cite: 1, 2].

---

## 2. A Ligação do GitHub com a Aula 2 da Semana 21: Pipeline de Feedback e Cultura DevOps

Na nossa disciplina, aprendemos sobre a **Cultura DevOps**, que busca unir quem desenvolve o sistema (Dev) e quem cuida da infraestrutura/operação (Ops) para entregar software com mais agilidade e qualidade[cite: 2].

O tema central da **Aula 2 (SISANO1C3B4S21A2)** é o **Pipeline de Feedback**[cite: 2]. Em termos simples, um pipeline de feedback é uma esteira automática que pega no código alterado, faz o *build* (compilação), executa os testes e devolve uma resposta rápida à equipa sobre o estado daquele código[cite: 7, 8].

### O Custo do Atraso e a Mentalidade *Fail Fast*
A regra de ouro que vimos na aula é: **quanto mais tempo demoramos para descobrir um erro, mais caro e complexo fica corrigi-lo**[cite: 9]. 
* Se um bug for descoberto em 2 minutos logo que o código é enviado, o aluno/desenvolvedor corrige-o na hora[cite: 6].
* Se o bug for para produção e ficar a falhar durante o fim de semana, o prejuízo e o retrabalho são enormes[cite: 6].

Por isso usamos a mentalidade ***fail fast*** (falhar rápido)[cite: 7, 12]: queremos que o sistema aponte qualquer erro o mais cedo possível. Trabalhar em **pequenos lotes** (fazer alterações pequenas e frequentes em vez de um código gigante de uma só vez) ajuda a equipa a receber feedback quase instantâneo[cite: 9].

---

## 3. Como os Recursos do GitHub Sustentam o Ciclo de Feedback

O GitHub não é só uma pasta na nuvem. Tem ferramentas que garantem tanto o **feedback humano** como o **feedback automatizado**[cite: 1, 2]:

### A. Issues (Feedback de Problemas e Ideias)
As **Issues** funcionam como um painel de recados e tarefas do projeto[cite: 8]. É onde qualquer membro da equipa ou utilizador regista um bug encontrado, sugere uma melhoria ou detalha uma nova tarefa. O feedback começa aqui, mapeando a necessidade antes de o código ser escrito.

### B. Pull Requests (Feedback Humano e Revisão por Pares)
Quando vamos enviar uma alteração para o projeto principal, criamos um **Pull Request (PR)**. O PR é a etapa de feedback humano: os colegas de equipa analisam o código, fazem comentários, sugerem mudanças na lógica e só aprovam quando tudo estiver correto. Isto evita que códigos com erros entrem diretamente na versão principal.

### C. GitHub Actions (Feedback Automatizado — Integração Contínua)
O **GitHub Actions** é a ferramenta que constrói o pipeline de feedback propriamente dito[cite: 8]. Sempre que alguém faz um commit ou abre um Pull Request, o GitHub Actions dispara um *workflow* (esteira) automatizado que tenta executar o projeto e corre os testes criados pela equipa[cite: 7, 8]. 
* Se os testes passarem, mostra um ícone verde de sucesso (badge)[cite: 7, 8].
* Se algum teste falhar, avisa imediatamente no ecrã, impedindo que o código defeituoso avance[cite: 7, 12].

---

## 4. Exemplo Prático: O Site de Horários da Turma

Para ficar bem claro como isto funciona na nossa rotina escolar do 2º CT, imagina que o nosso grupo está a desenvolver um **site de horários das aulas**:

1. **Problema identificado (Issue):** Um colega avisa que a aula de quarta-feira está com o horário errado no site e abre uma **Issue** a relatar o erro.
2. **Correção e Proposta (Pull Request):** O aluno responsável corrige a informação no seu código local e envia a mudança abrindo um **Pull Request**.
3. **Revisão da Equipa:** A dupla lê o código no PR, faz um comentário a pedir um ajuste de formatação e aprova.
4. **Verificação Automática (GitHub Actions):** O GitHub Actions executa automaticamente a esteira de testes e confirma que o layout não partiu.
5. **Entrega e Novo Ciclo:** A alteração é aprovada e vai para o ar. Os colegas usam o site e, se notarem algo novo, abrem outra Issue, reiniciando o ciclo de melhoria contínua.

---

## 5. Limites da Ferramenta e Considerações Finais

Apesar de o GitHub ser essencial, é importante entender os seus limites:

1. **Ferramenta não cria cultura sozinha:** Ter o GitHub configurado não significa ter Cultura DevOps. A cultura depende de comunicação, colaboração e compromisso da equipa.
2. **Testes aprovados não garantem 100% de perfeição:** Os testes automáticos só validam o que foram programados para testar. Um teste verde significa que o código passou nas regras criadas, mas não garante a ausência total de bugs não previstos.
3. **Necessidade de outras integrações:** Para monitorizar o sistema a executar na nuvem em tempo real (como uso de memória ou erros de servidor), muitas vezes precisamos de conectar o GitHub a ferramentas externas de monitorização.

---

## 6. Referências Consultadas

* **DORA.** *Working in small batches*. Disponível em: <https://dora.dev/capabilities/working-in-small-batches/>. Acesso em: 2026.
* **GITHUB DOCS.** *About issues*. Disponível em: <https://docs.github.com/en/issues/tracking-your-work-with-issues/learning-about-issues/about-issues>. Acesso em: 2026.
* **GITHUB DOCS.** *Continuous integration with GitHub Actions*. Disponível em: <https://docs.github.com/en/actions/get-started/continuous-integration>. Acesso em: 2026.
* **GITHUB DOCS.** *Reviewing proposed changes in a pull request*. Disponível em: <https://docs.github.com/en/pull-requests/how-tos/review-pull-requests/reviewing-proposed-changes-in-a-pull-request>. Acesso em: 2026.
* **MICROSOFT LEARN.** *Implement continuous feedback in DevOps*. Disponível em: <https://learn.microsoft.com/en-us/training/paths/az-400-implement-continuous-feedback/>. Acesso em: 2026.
* **SEDUC-SP.** *Desenvolvimento de Sistemas — 2º Ano CT: Cultura DevOps e feedback contínuo* (Código da Aula: SISANO1C3B4S21A2). São Paulo, 2026.
