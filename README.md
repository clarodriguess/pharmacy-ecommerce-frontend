# 💊 Pharmacy E-commerce — Frontend

Aplicação web desenvolvida em **React + TypeScript** para gerenciamento de produtos farmacêuticos, consumindo a [Pharmacy E-commerce API](https://github.com/clarodriguess/pharmacy-ecommerce-api) desenvolvida com NestJS. O sistema permite visualizar, cadastrar, editar e excluir produtos e categorias.

---

## 🔗 Repositórios do Projeto

| Camada | Repositório | Tecnologias |
|---|---|---|
| **Frontend** | [pharmacy-ecommerce-frontend](https://github.com/clarodriguess/pharmacy-ecommerce-frontend) | React · TypeScript · Tailwind |
| **Backend** | [pharmacy-ecommerce-api](https://github.com/clarodriguess/pharmacy-ecommerce-api) | NestJS · TypeORM · MySQL |

---

## 🚀 Tecnologias

| Tecnologia | Versão | Descrição |
|---|---|---|
| React | 19 | Biblioteca de UI |
| TypeScript | ~6.0 | Tipagem estática |
| Vite | 8 | Build tool e dev server |
| Tailwind CSS | 4 | Estilização utilitária |
| Axios | 1.15 | Requisições HTTP |
| React Router DOM | 7 | Roteamento SPA |
| Phosphor Icons | 2.1 | Biblioteca de ícones |
| React Spinners | 0.17 | Indicadores de carregamento |

---

## 📁 Estrutura do Projeto

```
src/
├── components/        # Componentes reutilizáveis (Navbar, Cards, Forms...)
├── pages/             # Páginas da aplicação
├── models/            # Interfaces TypeScript das entidades
├── services/          # Configuração do Axios e chamadas à API
└── App.tsx            # Configuração de rotas
```

---

## 🗂️ Entidades

### Produto

```ts
interface Produto {
  id: number;
  nome: string;
  descricao: string;
  preco: number;
  foto: string;
  categoria: Categoria;
}
```

### Categoria

```ts
interface Categoria {
  id: number;
  nome: string;
  descricao: string;
  produto?: Produto[];
}
```

> Uma **Categoria** pode conter vários **Produtos** (relacionamento 1:N).

---

## ⚙️ Como Rodar o Projeto

### Pré-requisitos

- Node.js 18+
- API backend rodando em `http://localhost:4000` → [veja como rodar a API](https://github.com/clarodriguess/pharmacy-ecommerce-api)

### Instalação

```bash
# Clone o repositório
git clone https://github.com/clarodriguess/pharmacy-ecommerce-frontend

# Entre na pasta
cd pharmacy-ecommerce-frontend

# Instale as dependências
npm install
```

### Executar em desenvolvimento

```bash
npm run dev
```

Acesse em: [http://localhost:5173](http://localhost:5173)

> ⚠️ Certifique-se de que a API está rodando antes de iniciar o frontend.

### Build para produção

```bash
npm run build
```

---

## 🔗 Endpoints Consumidos

### 📁 Categorias — `/categorias`

| Método | Rota | Descrição |
|---|---|---|
| GET | `/categorias` | Lista todas as categorias |
| GET | `/categorias/:id` | Busca categoria por ID |
| POST | `/categorias` | Cadastra nova categoria |
| PUT | `/categorias` | Atualiza categoria |
| DELETE | `/categorias/:id` | Remove categoria |

### 💊 Produtos — `/produtos`

| Método | Rota | Descrição |
|---|---|---|
| GET | `/produtos` | Lista todos os produtos |
| GET | `/produtos/:id` | Busca produto por ID |
| POST | `/produtos` | Cadastra novo produto |
| PUT | `/produtos` | Atualiza produto |
| DELETE | `/produtos/:id` | Remove produto |

---

## ✨ Funcionalidades

- [x] Listagem de produtos com informações detalhadas
- [x] Cadastro e edição de produtos
- [x] Exclusão de produtos
- [x] Listagem e gerenciamento de categorias
- [x] Relacionamento produto ↔ categoria
- [x] Feedback visual com loading spinners
- [x] Navegação entre páginas com React Router

---

## 👩‍💻 Autora

Desenvolvido por **Clarisse Rodrigues** como projeto final do Bloco 03 do Bootcamp FullStack - Generation Brasil

[![GitHub](https://img.shields.io/badge/GitHub-clarodriguess-181717?style=flat&logo=github)](https://github.com/clarodriguess)
