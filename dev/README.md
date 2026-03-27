# Dev Guide

Este diretório centraliza padrões de desenvolvimento e fluxo de trabalho.

## Fluxo de branches
- `main`: branch estável
- `dev`: integração contínua de features
- `feature/<nome>`: desenvolvimento de funcionalidade
- `hotfix/<nome>`: correções urgentes

## Convenções
- Commits curtos e descritivos
- Pull Request obrigatório para merge em `main`
- Cada feature deve ter sua própria pasta em `src/features`

## Checklist por feature
- Interface testada em desktop e mobile
- Eventos de câmera e permissão validados
- Performance com webcam revisada
- README atualizado quando necessário
