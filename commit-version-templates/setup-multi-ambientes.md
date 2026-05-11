# 🌍 Setup do Commit-and-Tag-Version em Diferentes Stacks

Embora o `commit-and-tag-version` seja uma ferramenta criada no ecossistema JavaScript (distribuída via NPM), ela é **agnóstica de linguagem**. Isso significa que ela pode analisar os commits, gerar o `CHANGELOG.md` e criar as tags do Git para projetos em Python, Dart, Java, ou qualquer outra stack.

## ⚠️ Requisito Universal
Independente da linguagem do seu backend ou frontend, você precisará ter o **Node.js** (e o `npm`) instalado na sua máquina ou ambiente de CI/CD para rodar o script.

---

## 🟡 JavaScript / TypeScript (Node.js, React, Angular)

Em projetos baseados em Node.js, a instalação é nativa e a ferramenta atualiza automaticamente o arquivo `package.json`.

**1. Instalação:**
```bash
npm install --save-dev commit-and-tag-version

```

**2. Configuração no `package.json`:**
Adicione o script para facilitar a execução:

```json
{
  "scripts": {
    "release": "commit-and-tag-version"
  }
}

```

**3. Execução:**

```bash
npm run release

```

---

## 🔵 Dart / Flutter

Projetos Flutter/Dart usam o `pubspec.yaml` para controle de versão em vez do `package.json`.

**1. Instalação:**
Na raiz do projeto Flutter, crie um `package.json` simples apenas para gerenciar esta ferramenta, ou instale-a globalmente, ou rode via `npx` sem instalar localmente.
A forma mais limpa é usar via `npx`:

**2. Configuração no `.versionrc.json`:**
Você precisa ensinar a ferramenta a atualizar o `pubspec.yaml`. Adicione isto ao seu `.versionrc.json`:

```json
{
  "bumpFiles": [
    {
      "filename": "pubspec.yaml",
      "type": "plain-text"
    }
  ]
}

```

**3. Execução:**

```bash
npx commit-and-tag-version

```

---

## 🐍 Python

Projetos Python geralmente controlam a versão no arquivo `pyproject.toml` ou `setup.py`.

**1. Configuração no `.versionrc.json`:**
Adicione a instrução para a ferramenta alterar o arquivo onde a versão do projeto Python fica armazenada. Exemplo usando `pyproject.toml`:

```json
{
  "bumpFiles": [
    {
      "filename": "pyproject.toml",
      "type": "plain-text"
    }
  ]
}

```

*(Nota: O tipo "plain-text" procura por um padrão básico de versão, como `version = "1.0.0"`, no arquivo indicado).*

**2. Execução:**

```bash
npx commit-and-tag-version

```

---

## ☕ Java (Maven / Gradle)

Projetos Java Enterprise gerenciam dependências com Maven (`pom.xml`) ou Gradle (`build.gradle`).

**1. Configuração no `.versionrc.json`:**
Para o Maven, adicione o `pom.xml`. Para o Gradle, adicione o `build.gradle`.

Exemplo para **Maven**:

```json
{
  "bumpFiles": [
    {
      "filename": "pom.xml",
      "type": "plain-text"
    }
  ]
}

```

Exemplo para **Gradle**:

```json
{
  "bumpFiles": [
    {
      "filename": "build.gradle",
      "type": "plain-text"
    }
  ]
}

```

**2. Execução:**
Na raiz do projeto Java, execute no terminal:

```bash
npx commit-and-tag-version

```

---

## 💡 Dica de Ouro: Testando sem causar danos (Dry Run)

Sempre que estiver configurando a ferramenta pela primeira vez em um projeto não-JavaScript, é recomendado fazer um teste antes de confirmar qualquer alteração. Use a flag `--dry-run`:

```bash
npx commit-and-tag-version --dry-run

```

Isso mostrará no terminal tudo o que a ferramenta *faria* (quais arquivos alteraria, como o changelog ficaria), mas sem efetivamente alterar nada no seu repositório.

```

```