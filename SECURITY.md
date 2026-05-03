# Política de Segurança — VisionFlow

## Versões Suportadas

| Versão | Suporte de segurança |
|---|---|
| `main` (última) | ✅ Suportada |
| branches antigas | ❌ Não suportadas |

## Política de Privacidade e Dados

O VisionFlow processa **apenas localmente** no navegador do usuário:

- Nenhuma imagem ou frame da webcam é enviado a servidores externos.
- Nenhuma biometria de mão é armazenada em banco de dados ou cookies.
- O `localStorage` é utilizado exclusivamente para preferências do usuário (configurações de calibração e templates Libras), sem dados biométricos.
- A câmera só é ativada após **consentimento explícito** do usuário.

## Reportar uma Vulnerabilidade

Se você encontrou uma vulnerabilidade de segurança no VisionFlow, **não abra uma issue pública**.

Envie um e-mail descrevendo:

1. Descrição da vulnerabilidade
2. Passos para reproduzir
3. Impacto potencial estimado
4. Sugestão de correção (opcional)

**Contato:** maximusmiguel68@gmail.com

Respondemos em até **72 horas** e publicaremos um patch de acordo com a gravidade:

| Gravidade | Prazo de patch |
|---|---|
| Crítica | 24–48 horas |
| Alta | 7 dias |
| Média/Baixa | Próxima release |

## O que NÃO constitui uma vulnerabilidade

- Erros de UX sem impacto de segurança
- Melhorias de performance
- Bugs funcionais sem exposição de dados

## Créditos

Reportes responsáveis serão reconhecidos no `CHANGELOG.md` com o crédito ao pesquisador (se autorizado).
