# Estudos S.A. — Fórum 💬📚

![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white&style=for-the-badge)
![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white&style=for-the-badge)
![Supabase](https://img.shields.io/badge/Supabase-Auth-3FCF8E?logo=supabase&logoColor=white&style=for-the-badge)
![React Router](https://img.shields.io/badge/React_Router-7-CA4245?logo=reactrouter&logoColor=white&style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow?style=for-the-badge)

Fórum da plataforma **Estudos S.A.**, um espaço para candidatos a concursos públicos trocarem materiais, tirarem dúvidas e formarem grupos de estudo. Complementa a aplicação principal ([front-end](https://github.com/moreiraDavi/estudos-sa-frontend) e [back-end](https://github.com/moreiraDavi/estudos-sa-backend)), que gera rotinas de estudo com IA.

---

## ✨ Funcionalidades

- **Cadastro e login** com e-mail e senha via **Supabase Auth**
- **Sessão persistente**: um `AuthContext` acompanha o estado de autenticação (`onAuthStateChange`)
- **Rotas protegidas**: o fórum só abre para usuários logados (`ProtectedRoute`)
- **Categorias de discussão**: Materiais de Estudo, Perguntas & Respostas, Notícias de Concursos, Networking & Grupos e Motivação & Bate-papo
- **Criação de tópicos** por categoria (título, conteúdo e tags), busca e notificações na barra superior
- Logout seguro

## 🗺️ Próximos passos (levantamento de requisitos)

Os requisitos completos estão em [`Requisitos_Forum_S.A.rtf`](Requisitos_Forum_S.A.rtf). Entre eles:

- Respostas em tópicos e moderação
- Upload, avaliação e download de materiais de estudo (PDFs, resumos, mapas mentais)
- Grupos de estudo com mini-fórum interno

## ⚙️ Tecnologias

- **React 19** + **Vite**
- **React Router 7**
- **Supabase** (autenticação)
- **CSS Modules**
- **React Icons**

## 📁 Estrutura

```
FORUM_SA/forum/src
├── backend/       # cliente do Supabase
├── components/    # Footer e ProtectedRoute
├── context/       # AuthContext (sessão do usuário)
└── pages/         # Home, Login, Register e Forum
```

## 🚀 Como rodar

```bash
cd FORUM_SA/forum
npm install
npm run dev
```

Crie um arquivo `.env` em `FORUM_SA/forum` com as credenciais do seu projeto Supabase:

```
VITE_SUPABASE_URL=...
VITE_SUPABASE_ANON_KEY=...
```
