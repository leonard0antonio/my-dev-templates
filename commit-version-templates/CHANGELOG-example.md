# 📄 Exemplo de Changelog Automático (`CHANGELOG.md`)

Este arquivo demonstra como a ferramenta `commit-and-tag-version` gera o documento final de histórico de versões, baseando-se nas regras de Conventional Commits e no seu arquivo `.versionrc.json`.

## 📌 O que é e Funcionalidades

O Changelog (Histórico de Alterações) é um documento vivo que lista todas as mudanças notáveis em cada versão do seu projeto.
* **Transparência:** Mantém usuários e outros desenvolvedores informados sobre o que há de novo, o que foi consertado e o que mudou sob o capô.
* **Rastreabilidade:** Cada versão inclui links diretos para os commits originais (caso o repositório esteja no GitHub/GitLab), facilitando auditorias.
* **Foco no que Importa:** Graças ao `.versionrc.json`, commits de manutenção (como `chore` ou `style`) não poluem a leitura, destacando apenas o que agrega valor real ao produto.

---

## 📄 Como o arquivo final se parecerá:

Abaixo, um exemplo de como o arquivo gerado automaticamente fica na raiz do seu projeto após algumas rodadas de desenvolvimento e lançamentos de versão.

*(Nota: Os links de hashes, como `a1b2c3d`, seriam links clicáveis para o commit no GitHub)*

***

# [1.1.0](https://github.com/seu-usuario/seu-repo/compare/v1.0.0...v1.1.0) (2026-05-11)

### ✨ Funcionalidades (Features)

* **carreira:** adiciona fluxo de mapeamento de features na plataforma ([a1b2c3d](https://github.com/seu-usuario/seu-repo/commit/a1b2c3d))
* **ui:** implementa dashboard de acompanhamento de métricas ([e4f5g6h](https://github.com/seu-usuario/seu-repo/commit/e4f5g6h))

### 🐛 Correções de Bugs (Bug Fixes)

* **sql:** corrige imprecisão na query que retorna métricas de consumo diário no Supabase ([j7k8l9m](https://github.com/seu-usuario/seu-repo/commit/j7k8l9m))
* **mobile:** repara renderização responsiva no emulador Android ([n0o1p2q](https://github.com/seu-usuario/seu-repo/commit/n0o1p2q))

### ♻️ Refatoração de Código

* **components:** corrige lógica renomeando a função `handleDeleteTicket` para `handleCreateTicket` no TypeScript ([r3s4t5u](https://github.com/seu-usuario/seu-repo/commit/r3s4t5u))

***

# 1.0.0 (2026-04-15)

### ✨ Funcionalidades (Features)

* **player:** cria motor de reprodução de áudio na web para o catálogo ([z9y8x7w](https://github.com/seu-usuario/seu-repo/commit/z9y8x7w))
* **auth:** implementa sistema inicial de login de usuários ([v6u5t4s](https://github.com/seu-usuario/seu-repo/commit/v6u5t4s))

### 📝 Documentação

* **readme:** adiciona instruções de setup inicial e estruturação profissional do repositório ([r3q2p1o](https://github.com/seu-usuario/seu-repo/commit/r3q2p1o))

***