# ⚙️ Configuração do Versionamento (`.versionrc.json`)

Este arquivo é o coração da automação do seu versionamento. Ele dita as regras para a ferramenta `commit-and-tag-version`, definindo exatamente como o seu `CHANGELOG.md` será gerado a partir do seu histórico de commits.

## 📌 O que é e Funcionalidades

O `.versionrc.json` (ou apenas `.versionrc`) é um arquivo de configuração que mapeia os tipos de commit que você utiliza para a estrutura visual do seu changelog. Suas principais funcionalidades são:
* **Filtragem de Ruído:** Permite esconder commits estruturais ou rotineiros que não são relevantes para as notas de lançamento.
* **Personalização Visual:** Organiza os commits do histórico em sessões claras com títulos customizados e emojis amigáveis.
* **Mapeamento Semântico:** Garante que a ferramenta reconheça corretamente quais tipos de commit devem ser agrupados.

## 🚀 Como Usar

1. Crie um arquivo chamado `.versionrc.json` na raiz do seu novo projeto.
2. Copie e cole o código JSON padrão disponibilizado abaixo.
3. Quando você rodar o comando de release (ex: `npx commit-and-tag-version`), a ferramenta lerá esse arquivo e montará o changelog automaticamente, separando as seções conforme as regras configuradas.

---

## 📄 O Template Padrão

Copie este bloco para dentro do seu arquivo `.versionrc.json`:

```json
{
  "types": [
    {"type": "feat", "section": "🚀 Novas Funcionalidades"},
    {"type": "fix", "section": "🐛 Correção de Bugs"},
    {"type": "style", "section": "🎨 Estilo & UI/UX", "hidden": false},
    {"type": "refactor", "section": "♻️ Refatoração de Código", "hidden": false},
    {"type": "perf", "section": "⚡ Melhorias de Performance", "hidden": false},
    {"type": "docs", "section": "📝 Documentação", "hidden": true},
    {"type": "chore", "section": "🔧 Manutenção", "hidden": true},
    {"type": "test", "section": "✅ Testes", "hidden": true}
  ]
}