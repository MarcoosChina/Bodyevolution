# Stitch Skills para o BodyEvolution

Este projeto agora está preparado para trabalhar com o ecossistema de habilidades do Stitch.

## Pré-requisito

As habilidades do Stitch dependem do Stitch MCP server configurado no ambiente do agente.

## Habilidades disponíveis

### stitch-design

- `stitch::code-to-design` – converter código frontend em design no Stitch.
- `stitch::generate-design` – gerar novas telas, editar telas existentes e criar variações.
- `stitch::manage-design-system` – enviar `DESIGN.md` e aplicar temas nas telas.
- `stitch::extract-design-md` – extrair um `DESIGN.md` a partir do código fonte.
- `stitch::extract-static-html` – extrair HTML estático de um app em execução.
- `stitch::upload-to-stitch` – enviar assets locais para um projeto Stitch.

### stitch-build

- `react-components` – converter telas do Stitch em componentes React.
- `react-native` – converter designs em componentes React Native.
- `remotion` – gerar vídeos de walkthrough a partir de projetos Stitch.
- `shadcn-ui` – orientar integração com shadcn/ui.

### stitch-utilities

- `design-md` – gerar `DESIGN.md` a partir de projetos Stitch.
- `enhance-prompt` – melhorar prompts de UI.
- `stitch-loop` – gerar sites multipágina com validação automática.
- `taste-design` – gerar guias visuais premium e anti-genéricos.

## Uso recomendado neste repositório

- Use `stitch::extract-static-html` para manter a página exportada como referência visual.
- Use `stitch::code-to-design` quando houver código frontend novo para sincronizar com o Stitch.
- Use `react-components` quando o próximo passo for evoluir a exportação estática para uma base React.
- Use `manage-design-system` sempre que houver mudanças de identidade visual ou tokens.

## Fonte

- Repositório upstream: [google-labs-code/stitch-skills](https://github.com/google-labs-code/stitch-skills)
