# ShowUp — Sistema de Gerenciamento de Portfólio

O **ShowUp** é uma plataforma web desenvolvida para centralizar e gerenciar portfólios de projetos voltados à área de tecnologia. A aplicação permite que usuários cadastrem, organizem e apresentem seus projetos de maneira profissional, visual e padronizada, trazendo praticidade e consistência para estudantes e profissionais que desejam expor sua evolução técnica.

Este projeto foi desenvolvido com foco em boas práticas de arquitetura, documentação, segurança e usabilidade, utilizando o ecossistema Firebase como base de backend.

---

## 📌 Objetivos

- Centralizar dados de usuários e seus projetos em uma única plataforma.
- Facilitar o registro, visualização e manutenção de portfólios.
- Aplicar modelagem de dados alinhada a uma arquitetura NoSQL.
- Demonstrar domínio prático de serviços BaaS (Backend as a Service).
- Atender requisitos acadêmicos de documentação e desenvolvimento.

---

## 🏗️ Arquitetura & Tecnologias

O ShowUp utiliza uma abordagem baseada em serviços, separando responsabilidades e garantindo escalabilidade e manutenção simplificada.

**Stack Principal:**
- **Firebase Authentication** – Autenticação e gerenciamento de usuários.
- **Cloud Firestore** – Armazenamento de dados estruturados (NoSQL).
- **Cloud Storage** – Hospedagem de arquivos/imagens.

**Diretrizes de Arquitetura:**
- Backend as a Service (BaaS)
- Clean Code e SRP (Single Responsibility Principle)
- Modularização em serviços
- Tratamento robusto de erros
- Regras de segurança (Firebase Security Rules)

---

## ✅ Requisitos Funcionais

- **Autenticação de Usuário**
- **Gestão de Perfil**
- **Criação, edição e exclusão de projetos**
- **Upload de imagens (JPG/PNG)**
- **Listagem de portfólio filtrada por usuário**
- **Visualização detalhada dos projetos**

---

## 🔐 Requisitos Não Funcionais

- **Segurança:** Acesso restrito aos dados do próprio usuário.
- **Performance:** Consultas otimizadas com índices e filtros.
- **Confiabilidade:** Tratamento de exceções nas operações críticas.
- **Manutenibilidade:** Código organizado por serviços e camadas.
- **Escalabilidade:** Uso de arquitetura NoSQL flexível.

---

## 🗂️ Modelagem de Dados (Firestore)

### Entidade: `users`
| Campo | Tipo | Descrição |
|-------|------|-----------|
| uid (PK) | String | Identificador único |
| name | String | Nome do usuário |
| email | String | Endereço de e-mail |
| bio | String | Descrição breve |

### Entidade: `projects`
| Campo | Tipo | Descrição |
|-------|------|-----------|
| id (PK) | String | ID do projeto |
| user_uid (FK) | String | Relacionamento com usuário |
| title | String | Título do projeto |
| description | String | Detalhamento técnico |
| technologies | Array<String> | Tecnologias utilizadas |
| main_image_url | String | URL da imagem principal |
| created_at | Timestamp | Data de criação |

---

## 🧩 Estrutura do Código

- `/services` — Regras de negócio e comunicação com Firebase
- `/components` — Componentes da interface
- `/pages` — Estrutura de telas
- `/assets` — Imagens e arquivos

---

## 📊 Status do Projeto

**Fase atual:** Desenvolvimento da interface e prototipação  
**Próximos passos:**
- Integração completa com Firestore
- Implementação do fluxo de edição de portfólio
- Testes e validação com usuários

---

## 📎 Público-Alvo

- Estudantes de tecnologia
- Desenvolvedores iniciantes
- Profissionais que desejam documentar sua evolução técnica

---

## 👤 Autor

**Gustavo Araújo Prchibiliski**  
Projeto acadêmico — Desenvolvimento de Sistemas.

---

## 📄 Licença

Projeto de uso educacional e demonstrativo.

