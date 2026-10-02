## Olá, eu sou a Julia 👋

Sou engenheira estudando desenvolvimento de software, com foco em
arquitetura: Clean Architecture, DDD, Design Patterns e testes automatizados, em
Python e TypeScript. Venho de experiências em lógica, automação e modelagem de dados e
estou expandindo para arquitetura de sistemas e desenvolvimento full-stack.

Cada repositório aqui é uma prova prática: a teoria só conta quando sai do papel,
com entregável testado, documentado e com as decisões por trás do código, incluindo
as limitações e os erros corrigidos pelo caminho.

**LinkedIn:** [linkedin.com/in/juliagasparin](https://www.linkedin.com/in/juliagasparin)


**Stack:** PostgreSQL · Python · FastAPI · Celery · Redis · TypeScript · React · Vite · Pytest · Vitest · GitHub Actions

---

### 🚀 Jornada

Cada linha leva direto à decisão de arquitetura mais relevante da etapa. (A Etapa 1
foi a configuração do ambiente e não gera entregável.)

| Etapa | Entregável | Decisão-chave |
| :---: | :--- | :--- |
| **2** | Modelagem relacional (agendamento médico e empréstimo de biblioteca) | Disponibilidade derivada por índice único parcial, em vez de uma flag booleana — [agendamento-medico](https://github.com/juliagasparin/agendamento-medico) · [emprestimos-biblioteca](https://github.com/juliagasparin/emprestimos-biblioteca#etapa-2--modelo-de-dados) |
| **3** | Clean Architecture e DDD em Python | [Invariante entre reserva e empréstimo garantida no domínio](https://github.com/juliagasparin/emprestimos-biblioteca#invariante-central), onde o banco não consegue |
| **4** | Strategy para o prazo de empréstimo | [Padrão aplicado só sobre regra real (fila de reserva), não sobre um conceito inexistente](https://github.com/juliagasparin/emprestimos-biblioteca#etapa-4--design-patterns-strategy) |
| **5** | Módulo de política de prazo em TypeScript | [Lógica de domínio portada para outra linguagem, com o escopo da prova de conceito assumido](https://github.com/juliagasparin/emprestimos-biblioteca#etapa-5--typescript) |
| **6** | Microsserviço de cálculo de prazo (FastAPI) | [Fallback para a política local quando o serviço remoto falha](https://github.com/juliagasparin/emprestimos-biblioteca#etapa-6--microsserviços) |
| **7** | Jobs com Celery e cache de disponibilidade com Redis | [Decorator de cache com TTL e invalidação explícita, e a revisão de um vazamento de infraestrutura](https://github.com/juliagasparin/emprestimos-biblioteca#etapa-7--processamento-assíncrono-e-cache) |
| **8** | Interface React consumindo a API | [Estado gerenciado à mão e contrato de dados tipado, sem biblioteca de data-fetching](https://github.com/juliagasparin/emprestimos-biblioteca#etapa-8--react-fatia-1-disponibilidade) |
| **9** | Testes automatizados e pipeline no GitHub Actions | [Integração com Postgres e Redis reais, fail-fast e branch protection na `main`](https://github.com/juliagasparin/emprestimos-biblioteca#etapa-9--cicd-e-testes-automatizados) |

---

### 🛠️ Repositórios

- **[emprestimos-biblioteca](https://github.com/juliagasparin/emprestimos-biblioteca):**
  um sistema de empréstimo de biblioteca evoluído etapa por etapa: do schema em
  PostgreSQL a Clean Architecture, microsserviço, cache, interface React e CI/CD.
- **[agendamento-medico](https://github.com/juliagasparin/agendamento-medico):**
  modelagem relacional em PostgreSQL com integridade garantida no banco (índices
  únicos parciais, `ON DELETE RESTRICT`) e constraints testadas com dados reais.

### 📖 Como ler

Os READMEs seguem a mesma estrutura: **Problema**, **Solução**, **Testado localmente**
e **Limitações conhecidas**.

