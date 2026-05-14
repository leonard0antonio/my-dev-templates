### 3. Prompt 06: `06-criacao-de-testes-qa.md`
Como a garantia de qualidade (QA) e os testes automatizados são fundamentais para um código robusto, este prompt acelera a criação de cenários de teste.

```markdown
# Prompt: Criação de Testes Automatizados (QA)

**Copie o texto abaixo e preencha as informações entre colchetes:**

---

Atue como um Engenheiro de Qualidade de Software (QA) e especialista em automação de testes. Preciso garantir a estabilidade do código abaixo.

**Ferramenta de Teste:** <Ex: Jest, Cypress, Flutter Test, Supertest>
**Tipo de Teste:** <Ex: Teste Unitário / Teste de Integração / Teste de Componente>

**Aqui está o código/função que precisa ser testado:**
```<linguagem>
<Cole aqui componente código, função o ou>

```

**Por favor, gere os casos de teste considerando o seguinte:**

1. **Caminho Feliz (Happy Path):** O cenário onde tudo funciona como o esperado.
2. **Casos Extremos (Edge Cases):** Teste entradas nulas, arrays vazios, formatos incorretos ou falhas de API.
3. Utilize a estrutura padrão de `describe` e `it` (ou equivalente na linguagem).
4. Adicione comentários explicando o que cada bloco de teste está validando.