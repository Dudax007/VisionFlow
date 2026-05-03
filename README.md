# VisionFlow

> Touchless UX com foco em privacidade para experiências web interativas.

O VisionFlow é um projeto de interface web para interação sem toque, usando visão computacional com webcam para capturar biometria das mãos e transformar gestos em ações de navegação.

## Visão do Projeto

O projeto utiliza um modelo de IA da linha Gemini para estratégia de biometria da mão e camada de inteligência da experiência, com implementação front-end em HTML + JavaScript.

Fluxo principal:
1. Captura da webcam em tempo real.
2. Detecção de landmarks da mão.
3. Mapeamento de gestos para cursor, clique e rolagem.
4. Feedback visual instantâneo na interface.

## Stack Atual

- HTML5
- JavaScript (Vanilla)
- MediaPipe Hands (detecção de landmarks)
- Gemini (camada de IA para evolução de biometria/experiência)

## Estrutura Profissional do Repositório

```text
VisionFlow/
├── .gitignore
├── README.md
├── dev/
│   └── README.md
├── docs/
│   └── README.md
└── src/
    ├── README.md
    └── features/
        ├── hand-biometrics/
        │   ├── index.html
        │   └── script.js
        └── libras/
            ├── index.html
            └── script.js
```

## Organização de Branches (Git)

- `main`: produção/estável.
- `dev`: integração contínua das funcionalidades.
- `feature/<nome-da-feature>`: desenvolvimento isolado de novas features.
- `hotfix/<nome-do-ajuste>`: correções urgentes.

Sugestão de fluxo:
1. Criar branch a partir de `dev`.
2. Implementar a feature em `src/features/<nome>`.
3. Abrir PR para `dev`.
4. Promover `dev` para `main` em release.

## Funcionalidades Implementadas

- Controle de cursor por movimento da mão.
- Clique por gesto de pinça.
- Scroll por posição vertical da mão.
- Feedback de status para usuário durante detecção.
- Onboarding guiado em 3 etapas (consentimento, detecção e clique).
- Banner de consentimento de câmera com revogação de captura.
- Fallback sem câmera por teclado (setas/WASD + Enter/Espaço).
- Painel de calibração ao vivo com presets (Suave, Padrão e Rápido).
- Histórico rápido de eventos em tempo real.
- Página web de hospedagem em `index.html` com preview da ferramenta.
- Pinça longa para alternar rapidamente o modo apresentação.
- Swipe lateral com a mão para navegar entre checkpoints da demo.
- Modo apresentação com foco visual para pitch e demonstração.
- Interpretador Libras experimental com alfabeto inicial por regras.
- Studio Libras dedicado em página separada com composição de frase, sugestões contextuais e templates personalizados.

## Como Executar

Como o projeto está em HTML e JavaScript puro, basta abrir:

- `index.html` (página de hospedagem principal)
- `src/features/hand-biometrics/index.html` (laboratório touchless direto)
- `src/features/libras/index.html` (studio dedicado de interpretação em Libras)

Para melhor experiência, use servidor local. Exemplo:

```bash
cd src/features/hand-biometrics
python3 -m http.server 5500
```

Depois, acesse `http://localhost:5500`.

## Como Contribuir

Para contribuir com padrao de qualidade e fluxo de PR, consulte:

- `CONTRIBUTING.md`

## Próximos Passos Recomendados

- Criar novas features em `src/features/` (ex.: privacidade adaptativa por face).
- Adicionar camada de configuração para provedores de IA.
- Formalizar testes manuais e checklist de QA em `docs/`.
