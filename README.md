# TESTE.Product

Olá,

Como parte do processo técnico, gostaríamos que você realizasse uma breve **tarefa prática** para avaliarmos seus conhecimentos em **C# / .NET**, **Entity Framework**, **boas práticas de arquitetura** e, de forma opcional, **CQRS** e **OData**.

Abaixo estão todas as instruções detalhadas:

---

### 🎯 **Objetivo**

Desenvolver uma **API REST** em **C# (.NET 8 ou superior)** para o gerenciamento de produtos e categorias, utilizando **Entity Framework Core com PostgreSQL** como banco de dados, seguindo boas práticas de **DDD (Domain-Driven Design)**.

O projeto deve demonstrar clareza, organização, uso adequado de camadas e uma boa modelagem de domínio.

---

### 🧱 **Requisitos Funcionais**

**Entidades principais:**

**Produto**

* `Id` (GUID)
* `Nome` (string, obrigatório)
* `Preço` (decimal, obrigatório)
* `CategoriaId` (GUID, obrigatório)
* `DataCadastro` (DateTime)

**Categoria**

* `Id` (GUID)
* `Nome` (string, obrigatório)

**Funcionalidades obrigatórias:**

* Criar, listar, editar e excluir **produtos**
* Criar e listar **categorias**
* Ao listar produtos, deve ser possível visualizar o **nome da categoria associada**

---

### ⚙️ **Requisitos Técnicos**

* **.NET 8+**
* **Entity Framework Core** com **PostgreSQL**
* Organização de código seguindo princípios de **DDD**
  (ex: camadas Domain, Application, Infrastructure e Api)
* Exposição de endpoints REST
* Utilização de **injeção de dependência**

---

### 💡 **Funcionalidades Opcionais (Bônus)**

Não são obrigatórias, mas serão valorizadas se implementadas:

* Padrão **CQRS** (separar comandos e queries)
* Implementar **OData** para listagens e filtros avançados
* Filtros de busca (por nome, categoria ou faixa de preço)
* Validações de domínio (ex: impedir preço negativo)
* Publicação de **eventos de domínio** (ex: ProdutoCadastradoEvent)
* Uso de **FluentValidation** para validação de entrada
* Exposição de **Swagger/OpenAPI**
* Testes unitários com **xUnit** ou **NUnit**
* Containerização com **Docker**

---

### 🧠 **Critérios de Avaliação**

Este exercício **não possui caráter eliminatório**, mas será utilizado para avaliar a qualidade e maturidade técnica do seu código.

Serão analisados com atenção os seguintes pontos:

| Critério                      | Descrição                                              |
| ----------------------------- | ------------------------------------------------------ |
| **Organização e arquitetura** | Estrutura clara de pastas e camadas                    |
| **Modelagem de domínio**      | Entidades e regras de negócio bem definidas            |
| **Uso do Entity Framework**   | Mapeamento, relacionamentos e uso correto do PostgreSQL     |
| **Qualidade do código**       | Clareza, nomes adequados, boas práticas e padronização |
| **Uso de padrões**            | DDD, CQRS (opcional), repositórios, serviços           |
| **Documentação**              | README explicativo e organizado                        |

---

### 🗂️ **Estrutura sugerida do projeto**

```
src/
 ├─ ProductCatalog.Api/
 │   ├─ Controllers/
 │   ├─ Program.cs
 │
 ├─ ProductCatalog.Application/
 │   ├─ Commands/
 │   ├─ Queries/
 │   ├─ DTOs/
 │
 ├─ ProductCatalog.Domain/
 │   ├─ Entities/
 │   ├─ ValueObjects/
 │   ├─ Events/
 │   ├─ Interfaces/
 │
 ├─ ProductCatalog.Infrastructure/
 │   ├─ Context/
 │   ├─ Mappings/
 │   ├─ Repositories/
 │
tests/
 ├─ ProductCatalog.Tests/
```

---

### 🚀 **Entrega**

* Crie uma **branch** específica para a sua entrega com o nome:

  ```
  demo/[seu-nome]
  ```

  *(Exemplo: `demo/leonardo-silva`)*
  

* Inclua um **README.[seu-nome].md** com:

  * Passos para rodar o projeto
  * Decisões técnicas e arquiteturais adotadas
  * (Opcional) Diagrama ou breve descrição da estrutura do projeto 

* Crie uma Pull Request para este Repositório

---

### 📅 **Prazos e Duração**

O tempo para a realização é livre — sugerimos entre **1 ou 2 dias s de dedicação**, mas você pode organizar conforme sua disponibilidade.

---

