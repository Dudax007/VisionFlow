# Contributing to VisionFlow

Obrigado por contribuir com o VisionFlow.
Este guia foi feito para facilitar contribuicoes com qualidade, previsibilidade e colaboracao.

## Sumario

- Objetivo do repositorio
- Stack e principios do projeto
- Fluxo de trabalho (Git)
- Como comecar localmente
- Padrao de branches
- Padrao de commits
- Pull Request (PR)
- Checklist de qualidade
- Boas praticas de codigo
- Regras de privacidade e seguranca
- Como reportar bugs e sugerir melhorias

## Objetivo do repositorio

O VisionFlow desenvolve uma experiencia web touchless com biometria de maos, priorizando:

- usabilidade em tempo real
- acessibilidade
- privacidade por padrao

## Stack e principios do projeto

Stack atual:

- HTML5
- JavaScript (vanilla)
- MediaPipe Hands
- Evolucao da camada de IA com Gemini

Principios:

- simplicidade primeiro
- feedback visual claro para usuario
- baixo acoplamento entre interface e logica de IA
- processamento local sempre que possivel

## Fluxo de trabalho (Git)

Modelo de branches:

- `main`: estado estavel
- `dev`: integracao de features
- `feature/<nome-curto>`: desenvolvimento de funcionalidade
- `hotfix/<nome-curto>`: correcao urgente

Fluxo recomendado:

1. Atualize a branch base (`dev`).
2. Crie sua branch de trabalho.
3. Implemente e valide localmente.
4. Abra PR para `dev`.
5. Ajuste comentarios de review.
6. Merge apenas apos aprovacao.

## Como comecar localmente

1. Clone o repositorio.
2. Acesse o diretorio da feature atual:

```bash
cd src/features/hand-biometrics
```

3. Rode servidor local:

```bash
python3 -m http.server 5500
```

4. Abra no navegador:

```text
http://localhost:5500
```

## Padrao de branches

Use nomes claros e curtos:

- `feature/cursor-smoothing`
- `feature/pinch-click-debounce`
- `feature/consent-banner`
- `hotfix/camera-permission-fallback`

## Padrao de commits

Preferencia: Conventional Commits.

Formato:

```text
<tipo>(<escopo>): <descricao curta>
```

Exemplos:

- `feat(tracking): adiciona suavizacao de cursor`
- `fix(click): evita duplo clique por ruido`
- `docs(readme): atualiza instrucoes de execucao`
- `chore(structure): organiza pastas de feature`

Tipos comuns:

- `feat`
- `fix`
- `docs`
- `chore`
- `refactor`
- `test`

## Pull Request (PR)

Titulo sugerido:

```text
[area] resumo objetivo da mudanca
```

Descricao minima do PR:

- Contexto: qual problema esta sendo resolvido
- Solucao: o que foi implementado
- Impacto: onde pode afetar
- Evidencias: prints, videos, logs ou checklist

Checklist minimo no PR:

- [ ] Branch criada a partir de `dev`
- [ ] Codigo revisado localmente
- [ ] Sem quebra de fluxo principal (cursor, clique, scroll)
- [ ] README/docs atualizados quando necessario
- [ ] Testes manuais executados

## Checklist de qualidade

Antes de pedir review:

- [ ] Camera inicia e trata erro de permissao
- [ ] Rastreio de mao esta estavel
- [ ] Clique por pinca sem duplicidade
- [ ] Scroll por gesto sem disparo involuntario continuo
- [ ] Interface com estados claros (aguardando, ativo, erro)
- [ ] Performance aceitavel em ambiente local

## Boas praticas de codigo

- Mantenha funcoes pequenas e objetivas.
- Evite logica de negocio espalhada na camada de UI.
- Centralize configuracoes (thresholds, debounce, sensibilidade).
- Nao use numeros magicos sem contexto.
- Priorize nomes descritivos para variaveis e funcoes.

Para HTML/CSS/JS:

- Evite estilos e scripts excessivamente acoplados.
- Prefira organizacao por responsabilidade.
- Garanta legibilidade para manutencao futura.

## Regras de privacidade e seguranca

- Nao armazenar biometria de mao por padrao.
- Nao enviar imagens da camera para terceiros sem consentimento explicito.
- Sempre informar ao usuario quando a camera estiver ativa.
- Tratar erros de permissao de forma clara e segura.

## Como reportar bugs e sugerir melhorias

Ao abrir uma issue, inclua:

- Comportamento atual
- Comportamento esperado
- Passos para reproduzir
- Ambiente (navegador, sistema, dispositivo)
- Evidencias (print/video/log, se possivel)

Para melhorias:

- descreva o ganho de UX/performace/privacidade
- indique impacto tecnico esperado
- proponha criterio de aceite

## Duvidas e alinhamento

Se tiver duvida de arquitetura ou prioridade:

1. Abra uma issue com tag de discussao.
2. Relacione com item do backlog em `docs/backlog-inicial.md`.
3. Aguarde alinhamento antes de implementar mudancas grandes.
