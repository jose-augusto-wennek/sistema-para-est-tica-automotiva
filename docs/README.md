# Ultra Legacy

**Aluno:** José Augusto Wennek Fiuza

Sistema web para gerenciamento de uma empresa de estética automotiva, com cadastro de clientes, veículos, serviços e agendamentos.

## 📚 Documentação

* [PRD](/docs/prd.md)
* [Architecture](/docs/architecture.md)

## 🎨 Protótipo

[Google Stitch](https://stitch.withgoogle.com/projects/17088217055424468959)

## 🛠️ Tecnologias

* HTML5
* CSS3
* JavaScript
* Bootstrap 5.3.3
* Bootstrap Icons 1.11.3
* Node.js / NPM
* JSON Server
* FIPE API v1
* Git / GitHub

## 💡 Justificativa

O **Bootstrap 5.3.3** foi escolhido por facilitar a criação de interfaces responsivas através de Grid, Flexbox e componentes prontos, como cards, botões, formulários e modais.

A **FIPE API v1** foi escolhida por fornecer dados reais de veículos e valores de referência. A consulta será realizada por **tipo, marca, modelo e ano**, complementando o cadastro dos veículos do sistema.

A placa será armazenada no cadastro, mas não será utilizada para consulta direta na FIPE API.

## 📋 Checklist

### RA1

* [x] ID01 — Protótipo responsivo
* [x] ID02 — Bootstrap Grid/Flexbox
* [x] ID03 — CSS Grid/Flexbox
* [x] ID04 — Componentes Bootstrap

### RA2

* [x] ID05 — Unidades relativas
* [x] ID06 — Design System
* [x] ID07 — Sass/SCSS
* [x] ID08 — Tipografia responsiva
* [x] ID09 — `object-fit`
* [x] ID10 — Imagens responsivas

### RA3

* [x] ID11 — Validação HTML
* [x] ID12 — REGEX
* [x] ID13 — Select, radio e checkbox
* [x] ID14 — LocalStorage

### RA4

* [x] ID15 — Node/NPM
* [x] ID16 — Git/GitHub
* [x] ID17 — README
* [x] ID18 — Organização de pastas
* [x] ID19 — ESLint/Prettier
* [x] ID20 — jQuery
* [x] ID21 — jQuery Mask

### RA5

* [x] ID22 — JSON Server
* [x] ID23 — Serviços e histórico
* [x] ID24 — FIPE API

## ▶️ Execução

```bash
npm install
npm run server
```

Depois, abra o projeto no navegador.

## 📁 Estrutura

```text
ultra-legacy/
├── docs/
│   ├── prd.md
│   └── architecture.md
├── src/
├── db.json
├── package.json
├── README.md
└── .gitignore
```
