# Direct Control · Consulta CNPJ

Aplicação web para consultar dados públicos de empresas (CNPJ) diretamente na base da Receita Federal, via API pública [publica.cnpj.ws](https://publica.cnpj.ws).

Site 100% estático (HTML + React via CDN, sem back-end e sem build) — os dados são sempre buscados em tempo real no momento da consulta, direto na fonte.

## Funcionalidades

- Consulta de CNPJ com validação de dígitos verificadores
- Resumo, dados completos (com busca) e JSON bruto
- Exportação em CSV e cópia de JSON/CNPJ
- Histórico local de consultas (salvo no navegador)
- Nova tentativa automática e timeout em caso de instabilidade da API
- Aviso de conexão offline

## Rodando localmente

Não é necessário instalar nada. Basta abrir o `index.html` no navegador, ou servir a pasta com qualquer servidor estático, por exemplo:

```bash
npx serve .
```

## Deploy

Este projeto está pronto para deploy no [Vercel](https://vercel.com) como site estático (sem framework, sem build command). Veja o passo a passo completo no guia enviado junto com este repositório.

## Estrutura

```
.
├── index.html      # aplicação completa (HTML + CSS + React/JSX via Babel standalone)
├── vercel.json     # configuração mínima de deploy estático
└── README.md
```

## Aviso

Os dados exibidos vêm de uma API pública de terceiros (publica.cnpj.ws), que replica informações da Receita Federal. A Direct Control não hospeda nem armazena esses dados em servidor próprio.
