# 🏷️ Padrões de Commit e Versionamento

Para manter o histórico do Git limpo, rastreável e permitir a geração automática de Changelogs, adoto o padrão de **Conventional Commits** em conjunto com a ferramenta **`commit-and-tag-version`** (sucessora do `standard-version`).

Esta pasta guarda as configurações prontas para serem plugadas em qualquer repositório.

## 📂 O que tem aqui?

* **`commit-convention.md`**: Um guia rápido (cheatsheet) das tags permitidas nas mensagens de commit. Ex: `feat:`, `fix:`, `chore:`, `docs:`, `test:`. Serve como consulta rápida.
* **`versionrc-template.md`**: O template de configuração JSON/JS para instruir o `commit-and-tag-version` sobre quais tipos de commit devem aparecer no changelog e quais devem acionar uma mudança de versão (Major, Minor, Patch).
* **`CHANGELOG-example.md`**: Uma demonstração de como o arquivo final gerado automaticamente deve se parecer.

## 🚀 Como usar

1. No seu projeto principal, instale a ferramenta de versionamento (ex: `npm i -D commit-and-tag-version`).
2. Copie a configuração do `versionrc-template.md` para criar o arquivo `.versionrc` na raiz do seu projeto.
3. Siga estritamente as regras de commit listadas no `commit-convention.md`.
4. Ao finalizar um ciclo de desenvolvimento, rode o script de release para gerar as tags e o changelog de forma mágica!