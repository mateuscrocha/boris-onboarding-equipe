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

Ou usar o script do projeto:

```sh
npm run dev
```

## Deploy

O projeto está preparado para deploy estático, sem etapa de build.

### Vercel

Se você conectar este repositório na Vercel:

- framework preset: `Other`
- build command: vazio
- output directory: `.`

O arquivo `vercel.json` já deixa a publicação pronta para uma navegação mais limpa.

### Qualquer host estático

Também funciona em qualquer host que publique HTML, CSS, JS e assets estáticos diretamente.

### EasyPanel

O projeto também está preparado para subir como `App Service` no EasyPanel usando `Dockerfile`.

Configuração sugerida:

- tipo de serviço: `App`
- source: repositório GitHub
- builder: `Dockerfile`
- porta do app: `80`
- command: vazio
- arguments: vazio
- environment: nenhum obrigatório

Fluxo sugerido no painel:

1. criar um projeto, por exemplo `boris`
2. adicionar um novo `App Service`
3. conectar o repositório `boris-onboarding`
4. deixar o EasyPanel usar o `Dockerfile` do projeto
5. configurar domínio e proxy apontando para a porta `80`
6. fazer o primeiro deploy

Se o domínio for interno, você pode publicar algo como `onboarding.seudominio.com` ou outro subdomínio restrito da operação.

## Repositório local

Para trabalhar neste projeto como repositório independente, use o `git` diretamente dentro desta pasta:

```sh
cd /Users/eu.rochamateus/Documents/Codex/AgentOS/spaces/boris/areas/produto/workspaces/boris-onboarding
git status
```
