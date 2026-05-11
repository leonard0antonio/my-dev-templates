# 🏷️ Convenção de Commits (Conventional Commits)

Este projeto adota o padrão de **Conventional Commits**. Essa é uma convenção simples para padronizar as mensagens de commit, tornando o histórico do repositório legível por humanos e máquinas.

## 📌 O que é e Funcionalidades

O padrão baseia-se em adicionar um prefixo estruturado em cada mensagem de commit. Suas principais funcionalidades e vantagens são:
* **Geração de Changelogs Automáticos:** Ferramentas como o `commit-and-tag-version` conseguem ler o histórico e montar as notas de versão automaticamente.
* **Navegação Histórica:** Facilita muito encontrar quando um bug foi introduzido ou quando uma funcionalidade subiu para produção.
* **Acionamento de CI/CD:** Pipelines podem ser configurados para rodar rotinas específicas (como deploy em buckets do S3 ou execução de automação de QA) dependendo do tipo do commit.
* **Comunicação Clara:** Transmite a intenção exata do código para outros desenvolvedores da equipe.

## 🚀 Como Usar

A estrutura básica de todo commit deve ser:

`<tipo>([escopo opcional]): <descrição clara e no imperativo>`

**Regras de Ouro:**
1. A descrição deve começar com letra minúscula.
2. Use o verbo no **imperativo** (ex: "adiciona", "corrige", "cria" em vez de "adicionado", "corrigindo").
3. Não coloque ponto final na descrição.

---

## 📚 Tipos de Commits e Exemplos

Aqui estão os prefixos aceitos no projeto, com exemplos de uso em situações reais:

### ✨ feat
Para desenvolvimento de novas funcionalidades, telas, fluxos ou integrações.
* `feat(home): adiciona nova tela de relatórios`
* `feat(player): cria motor de reprodução de áudio na web`
* `feat(auth): implementa integração com banco de dados PostgreSQL`

### 🐛 fix
Para resolução de bugs, erros de compilação ou falhas lógicas no sistema.
* `fix(login): corrige erro de autenticação`
* `fix(sql): corrige lógica da query que retorna métricas de consumo diário`
* `fix(ui): repara renderização responsiva no emulador Android`

### 💄 style
Para alterações que não afetam o significado do código (espaçamentos, formatação, CSS estético, ponto e vírgula). Não confundir com mudanças na lógica de UI.
* `style(perfil): ajusta padding e cores do card`
* `style(linter): remove aspas duplas e padroniza indentação no TypeScript`
* `style(navbar): alinha itens do menu lateral e ajusta tipografia`

### ♻️ refactor
Para alterações no código que não corrigem um bug nem adicionam uma funcionalidade, mas melhoram a estrutura, nomenclatura ou organização interna.
* `refactor(juridico): otimiza logica do StreamBuilder`
* `refactor(components): renomeia função handleDeleteTicket para handleCreateTicket no TypeScript`
* `refactor(db): centraliza as lógicas de CRUD e modelagem de dados`

### ⚡ perf
Para alterações de código focadas exclusivamente em melhorar a performance (tempo de resposta, consumo de memória, renderização).
* `perf(query): adiciona indexação para acelerar o tempo de resposta do banco`
* `perf(imagens): implementa lazy loading para otimizar o carregamento da página`
* `perf(api): reduz chamadas redundantes ao serviço de IAM`

### 📝 docs
Para inclusão ou alteração apenas em arquivos de documentação (README, Swagger, comentários em código).
* `docs(readme): atualiza instruções de setup do banco de dados no ambiente local`
* `docs(api): adiciona documentação detalhada das rotas do sistema de carreira`
* `docs(swagger): documenta payloads de entrada e saída para relatórios`

### 🔧 chore
Para tarefas de manutenção rotineiras, como atualização de dependências, configurações de build, ou modificações em arquivos ignorados (ex: `.gitignore`).
* `chore(deps): atualiza versão do React, Node.js e dependências gerais`
* `chore(cloud): configura arquivos base para integração de logs no CloudTrail`
* `chore(release): publica a versão 1.2.0 e gera changelog`

### 🧪 test
Para criação de novos testes, ajuste de testes existentes ou implementações focadas em Quality Assurance (QA).
* `test(auth): adiciona cenários de teste automatizado para validação de login`
* `test(components): cria testes unitários para a listagem de catálogos`
* `test(bug): implementa teste de regressão para garantir a geração correta de métricas`