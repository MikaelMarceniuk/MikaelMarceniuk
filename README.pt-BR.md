# Olá, eu sou o Mikael 👋

**Engenheiro Fullstack · 6+ anos · TypeScript, React/Next.js, Node.js/Bun, AWS**

🌎 **Aberto a oportunidades internacionais** · Remoto do Brasil (UTC-3, sobreposição com EUA e Europa) · Inglês: fluente

[![Portfólio](https://img.shields.io/badge/Portfólio-mmarceniuk.dev-0a0d14?style=flat&logo=vercel&logoColor=white)](https://mmarceniuk.dev)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mikael_Marceniuk-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mikael-marceniuk/)
[![Email](https://img.shields.io/badge/Email-mikael@mmarceniuk.dev-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:mikael@mmarceniuk.dev)

🇺🇸 [Read in English](README.md)

---

Entrei no desenvolvimento criando jogos na Unity3D e nunca parei. O que me prendeu não foi a tecnologia em si, mas a sensação de transformar uma ideia em algo que funciona. Hoje construo sistemas web, mobile e backend nos segmentos de apostas, automação enterprise e logística, e tenho conforto em assumir a entrega de ponta a ponta, das decisões de arquitetura até a produção.

## Destaques de impacto

- **Failover em tempo real na AWS.** Construí um sistema de failover automático em microserviços que detecta quedas de provedor e faz a troca em tempo real, mantendo disponível uma plataforma de apostas regulamentada.
- **Bilhões de registros, zero perda de dados.** Atuei em uma migração intercontinental da Europa para o Brasil usando AWS e Python.
- **~10% de crescimento de receita.** Desenvolvi um sistema de indicações fullstack em um time de 2 pessoas.
- **De 4 dias para 2 horas.** Projetei um pipeline de automação integrando 3 bancos de dados com Lecom, DocuSign e Feedz via REST APIs.
- **Milhões de linhas sem travar a API.** Arquitetei uma fila de mensagens na AWS para processar planilhas Excel de forma assíncrona em um produto da AbInBev, entregue solo em 2 semanas.

---

## Projetos em destaque

### [Collaborative Text Editor](https://collaborative-text-editor.mmarceniuk.dev/)

<img src="assets/collaborative-text-editor-mockup.webp" alt="Collaborative Text Editor" width="720">

Editor de documentos no estilo Google Docs simplificado, com editor rico, autosave e modo convidado. O produto é propositalmente simples, para o esforço ficar na engenharia de sincronização e persistência.

- Documentos modelados como **CRDT com Yjs**: o servidor recebe updates binários e faz o merge antes de persistir no MongoDB, então edições concorrentes convergem sem lock e sem last-write-wins.
- Escritas protegidas por concorrência otimista, e autosave com debounce, backoff exponencial e um flush final quando a aba fecha.
- Modo convidado: qualquer pessoa começa a escrever sem cadastro, e os documentos migram para a conta quando ela se registra.
- Monorepo com CI separado para web e server; um release só publica se os dois passarem (API no Fly.io, web na Vercel).

**Stack:** React, TypeScript, Tiptap, Yjs, Express, MongoDB, Better Auth, GitHub Actions<br>
**Links:** [Demo ao vivo](https://collaborative-text-editor.mmarceniuk.dev/) · [Código-fonte](https://github.com/MikaelMarceniuk/collaborative-text-editor)

### [Dalua.top](https://dalua.top/) · *Freelance*

<img src="assets/dalua-mockup.webp" alt="Dalua.top" width="720">

Loja virtual completa para uma marca de cuidados capilares: catálogo, carrinho, checkout com Mercado Pago, frete calculado pelo Melhor Envio e um painel onde a dona gerencia produtos, pedidos, cupons e conteúdo sem depender de um desenvolvedor.

- Roda numa hospedagem já contratada pelo cliente, com MySQL e sem acesso externo: as migrations são aplicadas automaticamente no boot do servidor, e o build roda no GitHub Actions e é publicado numa branch de deploy.
- Provedores de pagamento e frete conectados por **OAuth2** pela própria dona da loja, com tokens criptografados em **AES-256-GCM** e renovação dentro de uma transação com lock de linha, já que o refresh token é de uso único.
- Imagens convertidas para WebP no servidor e vídeos de depoimento convertidos no próprio navegador.

**Stack:** Next.js, TypeScript, MySQL, Drizzle, Better Auth, Mercado Pago, Melhor Envio, GitHub Actions<br>
**Links:** [Site ao vivo](https://dalua.top/) · Projeto de cliente, código privado

### [Higher Up Business English](https://higher-up.com.br/) · *Freelance*

<img src="assets/higher-up-mockup.webp" alt="Higher Up Business English" width="720">

Site institucional da única empresa no Brasil com metodologia BELF (Business English as a Lingua Franca), feito para ser encontrado no Google e transformar visitas em contatos.

- Páginas por solução e público (empresas, profissionais, startups, professores), para cada visitante cair numa página escrita para ele.
- Bilíngue (português e inglês) com next-intl e rotas por idioma, mais metadata, sitemap e robots gerados pela aplicação para o SEO.
- Analytics sem cookies com Umami, então o site não precisa de banner de consentimento. Publicado como imagem Docker construída pelo GitHub Actions.

**Stack:** Next.js, TypeScript, next-intl, Umami, Docker, GitHub Actions<br>
**Links:** [Site ao vivo](https://higher-up.com.br/) · Projeto de cliente, código privado

---

## Stack

**Frontend**<br>
![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-0F172A?logo=tailwindcss&logoColor=38BDF8)
![React Native](https://img.shields.io/badge/React_Native-20232A?logo=react&logoColor=61DAFB)

**Backend**<br>
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white)
![Bun](https://img.shields.io/badge/Bun-000000?logo=bun&logoColor=white)
![Elysia.js](https://img.shields.io/badge/Elysia.js-000000?logo=bun&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?logo=nestjs&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?logo=go&logoColor=white)
![GraphQL](https://img.shields.io/badge/GraphQL-E10098?logo=graphql&logoColor=white)

**Dados**<br>
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white)

**Cloud & DevOps**<br>
![AWS](https://img.shields.io/badge/AWS-232F3E?logo=amazonaws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?logo=terraform&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?logo=vercel&logoColor=white)

---

## Fora do código

Estudo teatro, atualmente no terceiro ano, com foco em teatro contemporâneo. Isso molda como penso sobre comunicação, no palco e em um time.

Leio bastante, principalmente livros de programação, livros sobre como lidar com pessoas e ficção de terror e detetive. No momento estou lendo *A Philosophy of Software Design*, *The Pragmatic Programmer* e *Never Split the Difference*. Favoritos recentes: *Na Escuridão da Mente*, de Paul Tremblay, e *O Bom Filho*, de You-jeong Jeong.

Também estudo russo (B2) e japonês (A1) ao mesmo tempo, porque aparentemente gosto de sistemas complexos.
