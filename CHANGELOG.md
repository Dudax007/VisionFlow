# Changelog — VisionFlow

Todas as mudanças notáveis neste projeto serão documentadas aqui.

Formato baseado em [Keep a Changelog](https://keepachangelog.com/pt-BR/1.0.0/),
e este projeto adere ao [Versionamento Semântico](https://semver.org/lang/pt-BR/).

---

## [Não lançado]

### Adicionado
- Página de hospedagem principal (`index.html`) com preview integrado do laboratório touchless
- Módulo completo **Studio Libras** (`src/features/libras/`) com:
  - Motor de reconhecimento de sinais por regras geométricas
  - Sistema de templates customizados com gravação ao vivo
  - Composição de frases com sugestões contextuais por prefixo
  - Exportação de transcrição como TXT
  - Modo alto contraste acessível
  - Atalhos de teclado (Alt+S, Alt+B, Alt+L, Alt+R, Alt+C)
- **Motor de rastreio Hand Biometrics** completamente refatorado:
  - Cursor EMA adaptativo (suavização dinâmica baseada em delta)
  - Pinça 3D com peso no eixo Z, histerese, debounce e cooldown
  - Scroll por zona neutra configurável (38%–62%)
  - Painel de calibração ao vivo (suavização, limiar de pinça, velocidade de scroll)
  - Métricas em tempo real (FPS, confiança, cliques, scrolls, uptime da mão)
  - Fallback por teclado (WASD/setas + Enter/Espaço)
  - Modal de consentimento de câmera com opção de recusa
  - Persistência de configurações via `localStorage`
  - Visualização de landmarks da mão (togglável)
  - Efeitos visuais de onda no clique (canvas)

### Alterado
- `README.md` atualizado com estrutura completa do projeto e todas as funcionalidades implementadas

### Infraestrutura
- `.gitignore` profissionalizado (`.env*`, `node_modules/`, editores, ferramentas de IA)
- `.editorconfig` adicionado para padronizar estilo entre editores
- `.prettierrc` adicionado para formatação consistente de código
- `SECURITY.md` adicionado com política de segurança e privacidade
- Branch `dev` criada como base de integração contínua

---

## [0.1.0] — 2025 (estado inicial)

### Adicionado
- Estrutura inicial do repositório
- Protótipo HTML touchless com MediaPipe Hands
- Controle básico de cursor por movimento da mão
- Clique por gesto de pinça (versão inicial)
- Scroll por posição vertical da mão (versão inicial)
- README inicial com visão do projeto
- Backlog inicial com 6 Epics em `docs/backlog-inicial.md`
- `CONTRIBUTING.md` com guia de contribuição e padrões de commit
