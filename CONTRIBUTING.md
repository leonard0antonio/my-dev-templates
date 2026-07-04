### 2. `CONTRIBUTING.md` (Guia de Contribuição)

Este arquivo é o manual que ensina de forma prática como um novo membro ou desenvolvedor de fora pode baixar o projeto, criar uma branch, submeter alterações e rodar os testes. Lembra que nós deixamos um link para ele no final dos seus templates de README? É este cara aqui!

```markdown
# 🚀 Guia de Contribuição

Primeiramente, obrigado por se interessar em contribuir com este projeto! São pessoas como você que fazem a comunidade open-source avançar.

Para manter a organização e a qualidade do código, pedimos que siga as diretrizes abaixo.

## 🛠️ Como Começar

1. Faça um **Fork** deste repositório.
2. Clone o seu fork na sua máquina local:
   ```bash
   git clone [https://github.com/seu-usuario/nome-do-projeto.git](https://github.com/seu-usuario/nome-do-projeto.git)

```

3. Crie uma branch para a sua modificação, utilizando nomes descritivos:
```bash
# Para novas funcionalidades:
git checkout -b feature/nome-da-feature
# Para correção de erros:
git checkout -b fix/nome-do-bug

```

## 🏷️ Padrão de Commits

Este repositório adota estritamente o padrão de **Conventional Commits**. Certifique-se de que todas as suas mensagens sigam a estrutura:

* `feat(escopo): descrição` para novas funcionalidades.
* `fix(escopo): descrição` para correções.
* Consulte o nosso guia interno `commit-convention.md` para a lista completa de tags aceitas.

## 📥 Submetendo Alterações

1. Certifique-se de rodar o linter e os testes locais antes de enviar o código.
2. Faça o push da sua branch para o seu fork:
```bash
git push origin feature/nome-da-feature

```


3. Abra um **Pull Request** detalhado apontando para a nossa branch principal (`main`).
4. Preencha o formulário padrão de Pull Request explicando suas motivações e anexando evidências visuais (se houver).
