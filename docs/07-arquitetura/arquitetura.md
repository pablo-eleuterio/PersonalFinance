# Arquitetura de Software — Personal Finance

## 1. Visão Geral
O Personal Finance será uma aplicação web Full Stack, desenvolvida com arquitetura monolítica modular, organizada por funcionalidades e com separação de responsabilidades em camadas.

O frontend e o backend serão independentes e se comunicarão por meio de uma API REST.

## 2. Tecnologias
| Categoria      | Tecnologia                   |
| -------------- | ---------------------------- |
| Backend        | Java 21, Spring Boot e Maven |
| Frontend       | React e TypeScript           |
| Banco de Dados | MySQL                        |
| Persistência   | Spring Data JPA              |
| Migrações      | Flyway                       |
| Segurança      | Spring Security              |
| Testes         | JUnit e Mockito              |
| Versionamento  | Git e GitHub                 |
| Infraestrutura | Docker e GitHub Actions      |

Docker e GitHub Actions serão implementados em etapas posteriores.

## 3. Organização do Sistema
O backend será organizado por funcionalidades, como usuários, contas financeiras, categorias, transações e metas.

Cada funcionalidade utilizará as responsabilidades necessárias:

* **Controller:** recebe requisições HTTP.
* **Service:** executa as regras de negócio.
* **Repository:** acessa o banco de dados.
* **Entity:** representa os dados persistidos.
* **DTO:** transporta os dados necessários.

O frontend será organizado em componentes e funcionalidades reutilizáveis.

## 4. Comunicação e Segurança
A comunicação entre React e Spring Boot utilizará API REST, HTTP e JSON.

O Spring Security será utilizado para autenticação e autorização, garantindo que cada usuário acesse apenas seus próprios dados.

As senhas serão armazenadas utilizando algoritmos seguros de hash.

A estratégia de gerenciamento de sessão será definida antes da implementação da autenticação.

## 5. Banco de Dados
O MySQL será utilizado como banco de dados relacional, seguindo os modelos MER e DER documentados.

O Spring Data JPA será responsável pela persistência e o Flyway pelo versionamento das alterações do esquema do banco.

## 6. Estrutura do Repositório

```text
personal-finance/
├── backend/
├── frontend/
├── database/
├── docs/
├── README.md
└── .gitignore
```

As estruturas internas serão criadas durante a implementação.

## 7. Estratégia de Desenvolvimento

O desenvolvimento será incremental, seguindo a ordem dos protótipos.

Cada tela será implementada de ponta a ponta, incluindo frontend, backend, banco de dados, integração e testes, antes de avançar para a próxima.

Dependências técnicas poderão ser implementadas antecipadamente quando necessário.

O versionamento seguirá o padrão Conventional Commits, com commits pequenos, descritivos e organizados por alterações relacionadas.

As alterações serão publicadas no GitHub após verificação do código e execução dos testes aplicáveis.

O desenvolvimento priorizará segurança, qualidade, manutenção e simplicidade, evitando complexidade desnecessária.
