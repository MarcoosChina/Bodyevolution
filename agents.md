# Agents Manual – BodyEvolution

Este documento serve como manual de instruções e configuração para os **agentes de Inteligência Artificial** utilizados no projeto BodyEvolution. Ele descreve o propósito de cada agente, como configurá‑los, boas práticas de uso e diretrizes de formatação de conteúdo que evitam erros de lint.

---

## 1. Visão Geral

- **Objetivo**: Auxiliar na automação de tarefas de desenvolvimento, geração de conteúdo e suporte ao usuário dentro do repositório.
- **Ambiente**: Os agentes operam no mesmo workspace que o usuário, com acesso a ferramentas de leitura/escrita de arquivos, busca de código (`glob`, `grep`) e execução de comandos (`bash`).
- **Comunicação**: Interagem via mensagens de texto. Respostas devem ser claras, concisas e focadas na ação solicitada.

## 2. Tipos de Agentes

- **Assistente**: responder perguntas, revisar código e gerar documentação. Uso típico: suporte geral ao desenvolvedor.
- **Explorador**: pesquisar rapidamente o código‑base com `glob` e `grep`. Uso típico: encontrar arquivos, trechos ou símbolos.
- **Executor**: realizar mudanças de código e commits. Uso típico: implementar funcionalidades ou correções.

> **Nota:** Cada agente respeita as permissões do usuário e deve solicitar confirmação antes de efetuar alterações permanentes.

## 3. Configuração

1. **Instalação** – Não é necessário instalar nada adicional; os agentes já estão disponíveis no ambiente OpenCode.
2. **Variáveis de ambiente** – Caso precise de chaves externas (por exemplo, `OPENAI_API_KEY`), defina‑as no terminal antes de iniciar a sessão.
3. **Arquivos de configuração** – Opcionalmente, inclua um arquivo `.markdownlint.jsonc` na raiz do projeto para customizar regras de lint (ex.: desativar `MD060`). Exemplo:

```json
{
  "default": true,
  "MD060": false
}
```

## 4. Boas Práticas de Formatação (Evitar erros MD060)

- **Alinhar colunas de tabelas**: Todas as linhas de uma tabela devem ter o mesmo número de caracteres entre os pipes (`|`). Use espaços de preenchimento para garantir que cada pipe fique na mesma coluna.
- **Usar separador consistente**: A linha de separação (`|---|---|`) deve ter **pelo menos três hífens** por coluna e **o mesmo comprimento** que o cabeçalho.
- **Exemplo de tabela alinhada**:

```markdown
| ID | Título                     | Descrição                     | Prioridade | Status |
|----|---------------------------|------------------------------|------------|--------|
| 1  | Exemplo de Funcionalidade  | Texto resumido da tarefa      | Alta       | TODO   |
| 2  | Exemplo de Bug            | Texto resumido do bug         | Média      | TODO   |
| 3  | Estruturar projeto Stitch | Migrar página estática para app | Alta    | TODO   |
```

- **Quebrar linhas longas**: Quando o conteúdo de uma célula excede o comprimento desejado, faça a quebra em linhas separadas ou use descrições resumidas.
- **Validar com markdownlint**: Rode `markdownlint .` antes de realizar commit para garantir que a formatação esteja correta.

## 5. Fluxo de Trabalho Recomendada

1. **Planejamento** – Atualize `backlog_mvp.md` com as listas de tarefas.
2. **Implementação** – Use o agente **Executor** para aplicar alterações de código.
3. **Revisão** – Solicite ao agente **Assistente** que revise as mudanças e execute novamente o lint.
4. **Commit** – O agente **Executor** cria o commit com uma mensagem clara e concisa.

## 6. Stitch Skills

Quando o projeto exigir geração, extração ou conversão visual ligada ao Stitch, consulte [stitch-skills.md](stitch-skills.md) para saber quais habilidades estão disponíveis e quais pré-requisitos precisam estar ativos.

---

*Este manual deve ser mantido atualizado à medida que novos agentes são introduzidos ou as políticas de codificação mudam.*
