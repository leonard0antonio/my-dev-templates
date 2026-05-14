# Prompt: Modelagem de Dados e Banco

**Copie o texto abaixo e preencha os colchetes:**

---

Atue como um Engenheiro de Dados e Administrador de Banco de Dados (DBA) Sênior. Preciso estruturar a camada de dados de uma nova aplicação.

**Sobre o Sistema:**
O sistema é um <ex: aplicativo de streaming de áudio / plataforma de relatórios corporativos / sistema de gestão de carreira>. 

**Principais entidades e regras de negócio que pensei até agora:**
- <Ex: Usuários (que podem ser Admin ou Comum)>
- <Ex: Catálogo de Músicas (que pertencem a Álbuns)>
- <Ex: Relatórios de Consumo Diário>

**O banco de dados escolhido é o <Ex: PostgreSQL / MySQL / Supabase / MongoDB>.**

**Por favor, gere:**
1. O **Diagrama Entidade-Relacionamento (MER)** detalhado em formato texto, explicando as cardinalidades (1:1, 1:N, N:M).
2. O script `SQL` (ou o schema do Prisma/Mongoose, dependendo do banco) completo para criação das tabelas, incluindo:
   - Chaves Primárias (PK) e Estrangeiras (FK).
   - Tipagem correta e otimizada dos dados.
   - Restrições (NOT NULL, UNIQUE, DEFAULT, exclusão em cascata).
   - Timestamps básicos (`created_at`, `updated_at`).
3. Sugira de 1 a 2 **índices (indexes)** que fariam sentido para otimizar as consultas mais comuns que esse sistema teria.