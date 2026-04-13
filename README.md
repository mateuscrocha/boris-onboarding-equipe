# Bóris Onboarding

Aplicativo interno de onboarding da equipe do Bóris.

Este projeto vive como um repositório próprio, separado das outras superfícies do ecossistema.

Este workspace existe para concentrar:

- visão geral do ecossistema Bóris
- trilha de entrada de novas pessoas do time
- mapa de papéis e responsáveis
- ferramentas, rituais e combinados internos
- FAQs e playbooks de apoio

## Papel no ecossistema

O `boris-onboarding` não faz parte do site público.

Ele é uma superfície interna, separada do:

- `boris-site`, que continua sendo a camada pública
- `boris-painel`, que continua sendo a camada autenticada do produto

Ele existe para ajudar quem entra no time a entender:

- o que é o Bóris
- em que momento o projeto está hoje
- quem são as pessoas envolvidas
- como começar a contribuir desde a primeira semana

## Estrutura

Este primeiro recorte foi feito como app estático para facilitar iteração rápida.

Arquivos principais:

- `index.html`
- `styles.css`
- `app.js`

## Como abrir localmente

Você pode servir este diretório com um servidor estático simples, por exemplo:

```sh
python3 -m http.server 8090
```

Depois acesse:

```txt
http://localhost:8090
```

## Repositório local

Para trabalhar neste projeto como repositório independente, use o `git` diretamente dentro desta pasta:

```sh
cd /Users/eu.rochamateus/Documents/Codex/AgentOS/spaces/boris/areas/produto/workspaces/boris-onboarding
git status
```
