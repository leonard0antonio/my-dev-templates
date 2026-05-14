# 🏷️ Padrões de Commit e Versionamento

Para manter o histórico do Git limpo, rastreável e permitir a geração automática de Changelogs, adoto o padrão de **Conventional Commits** em conjunto com a ferramenta **`commit-and-tag-version`** (sucessora do `standard-version`).

Esta pasta guarda as configurações prontas e os guias necessários para plugar esse fluxo de qualidade em qualquer repositório.

## 📂 O que tem aqui?

* [**`commit-convention.md`**](./commit-convention.md): Um guia rápido (cheatsheet) das tags permitidas nas mensagens de commit (`feat:`, `fix:`, `chore:`, etc). Serve como consulta rápida no dia a dia.
* [**`versionrc-template.md`**](./versionrc-template.md): O template de configuração JSON (`.versionrc.json`) para instruir a ferramenta sobre quais tipos de commit devem aparecer no changelog e suas respectivas seções.
* [**`CHANGELOG-example.md`**](./CHANGELOG-example.md): Uma demonstração de como o arquivo de notas de versão gerado automaticamente deve se parecer.
* [**`setup-multi-ambientes.md`**](./setup-multi-ambientes.md): Guia passo a passo para instalar e configurar o `commit-and-tag-version` em diferentes stacks e linguagens (Node.js, Dart/Flutter, Python, Java).
* [**`execucao-e-push.md`**](./execucao-e-push.md): O manual do dia a dia ensinando como rodar o comando de release e como fazer o push corretamente enviando as tags para o GitHub.

## 🚀 Como usar

1. Siga as instruções do [**`setup-multi-ambientes.md`**](./setup-multi-ambientes.md) para instalar a ferramenta no seu projeto atual.
2. Copie a configuração do [**`versionrc-template.md`**](./versionrc-template.md) para criar o arquivo `.versionrc.json` na raiz do projeto.
3. Durante o desenvolvimento, siga estritamente as regras de commit listadas no [**`commit-convention.md`**](./commit-convention.md).
4. Ao finalizar um ciclo de desenvolvimento (sprint), consulte o [**`execucao-e-push.md`**](./execucao-e-push.md) para rodar o script de release, gerar o changelog e subir a nova versão para o GitHub!

