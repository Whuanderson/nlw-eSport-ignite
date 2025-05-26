# NLW eSports – Ignite 🎮

<p align="center">
  <img src="https://raw.githubusercontent.com/Whuanderson/nlw-eSport-ignite/refs/heads/main/.github/cover.png" alt="NLW eSports cover" />
</p>

<p align="center">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/Whuanderson/nlw-eSport-ignite">
  <a href="https://www.linkedin.com/in/whuanderson-de-sousa-porto-marinho-a07204216/" target="_blank">
    <img alt="Made by Whuanderson" src="https://img.shields.io/badge/Made%20by-Whuanderson-purple">
  </a>
  <img alt="License" src="https://img.shields.io/badge/License-MIT-purple">
</p>

Aplicação full‑stack construída durante o **Next Level Week – eSports (Ignite)** da Rocketseat.  
O objetivo é ajudar gamers a **encontrar duos** para partidas online: crie um anúncio dizendo que procura companhia para jogar e receba o contato (Discord) de quem se interessar.

---

## 📦 Monorepo

| Pasta   | Descrição                         | Tecnologias principais |
|---------|-----------------------------------|------------------------|
| `web`   | Front‑end responsivo              | React • Vite • TypeScript • TailwindCSS |
| `mobile`| App mobile                        | React Native • Expo • TypeScript |
| `server`| API REST + WebSocket              | Node.js • Fastify • Prisma ORM • SQLite |

---

## ✨ Funcionalidades

- Cadastro/listagem de **jogos** populares  
- **Criação de anúncios** (nome, horário, Discord etc.)  
- Busca de anúncios por jogo  
- Recupera **ID do Discord** para contato via WebSocket em tempo real  
- Layout e componentes acessíveis e responsivos (web + mobile)

---

## 🚀 Executando localmente

> Requer **Node >= 18** e **Yarn** (ou npm).

```bash
# clone o repositório
git clone https://github.com/Whuanderson/nlw-eSport-ignite
cd nlw-eSport-ignite
```

### 1. Back‑end

```bash
cd server
yarn            # instala dependências
npx prisma migrate dev  # cria o banco SQLite
yarn dev        # inicia em http://localhost:3333
```

### 2. Web

```bash
cd ../web
yarn
yarn dev        # abre em http://localhost:5173
```

### 3. Mobile

```bash
cd ../mobile
yarn
npx expo start  # escaneie o QR code no Expo Go ou rode emulador
```

> Certifique‑se de alterar a URL da API no arquivo `mobile/src/lib/axios.ts` para apontar para o IP da sua máquina (ex.: `http://192.168.0.x:3333`).

---

## 🗂️ Estrutura

```
.
├─ server
│  ├─ prisma         # schema & migrations
│  └─ src
│     ├─ routes
│     ├─ controllers
│     └─ websocket
├─ web
│  └─ src
│     ├─ components
│     ├─ pages
│     └─ services
└─ mobile
   └─ src
      ├─ components
      ├─ screens
      └─ lib
```

---

## 📝 Licença

Este projeto está sob a licença **MIT**. Veja o arquivo [LICENSE](./LICENSE) para detalhes.

<p align="center">
  Feito por <a href="https://github.com/Whuanderson">Whuanderson Marinho</a> – deixe uma ⭐️ para apoiar!
</p>
