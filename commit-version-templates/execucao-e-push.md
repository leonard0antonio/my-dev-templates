# 🚀 Como Executar o Versionamento e Fazer Push para o GitHub

Depois de configurar o seu `.versionrc.json` e fazer os seus commits seguindo o padrão Conventional Commits, chega o momento de gerar a sua versão (release) e enviar tudo para o repositório remoto.

## 1️⃣ A Primeira Execução (First Release)

Se este for o **primeiro** lançamento do seu projeto, você não quer que a ferramenta aumente a versão atual (geralmente `1.0.0` ou `0.1.0`), apenas que ela gere o primeiro `CHANGELOG.md` e crie a tag inicial.

Execute no terminal:
```bash
npx commit-and-tag-version --first-release

```

*O que isso faz:* Gera o `CHANGELOG.md` com todos os commits feitos até o momento, altera os arquivos de configuração (se houver) e cria a primeira tag no Git (ex: `v1.0.0`), sem calcular salto de versão.

---

## 2️⃣ Execuções de Rotina (Standard Release)

Para o seu dia a dia, após finalizar uma funcionalidade, corrigir bugs ou terminar um ciclo de desenvolvimento (sprint), você rodará o comando padrão:

```bash
npx commit-and-tag-version

```

*(Se estiver em um projeto Node.js e configurou o script no `package.json`, pode usar `npm run release`)*

*O que isso faz:*

1. Analisa o histórico de commits desde a última tag.
2. Decide qual será a nova versão baseada nos prefixos (ex: `fix` = Patch, `feat` = Minor, `BREAKING CHANGE` = Major).
3. Atualiza os arquivos de configuração (como `package.json` ou `pubspec.yaml`) com o novo número.
4. Gera o bloco da nova versão no `CHANGELOG.md`.
5. Cria um commit automático com a mensagem `chore(release): X.X.X`.
6. Cria uma **Tag do Git** apontando para esse commit.

---

## 3️⃣ Fazendo o Push Correto para o GitHub

**Atenção:** Um `git push` normal **NÃO** envia as tags para o GitHub por padrão. Para garantir que suas tags de versão apareçam na aba "Releases / Tags" do GitHub, você precisa usar uma flag especial.

Sempre que rodar o processo de release, faça o push utilizando:

```bash
git push --follow-tags origin main

```

*(Troque `main` pelo nome da sua branch atual, caso esteja usando `master` ou outra branch de produção).*

### Por que `--follow-tags`?

Esse comando diz ao Git: "Envie os meus commits normais, mas envie também as Tags anotadas que estão atreladas a esses commits". Isso mantém o seu repositório remoto 100% sincronizado com a sua máquina local.

---

## 🔄 Resumo do Fluxo de Trabalho (Cheatsheet)

Para colar no seu monitor e não esquecer mais o ciclo completo:

```bash
# 1. Adicione seus arquivos alterados
git add .

# 2. Faça o commit usando o padrão definido
git commit -m "feat(relatorios): adiciona exportacao para PDF"

# 3. Rode a ferramenta de release (ao final da etapa/sprint)
npx commit-and-tag-version

# 4. Envie tudo para o GitHub, incluindo a nova tag!
git push --follow-tags origin main

```