# 💊 Farmácia React — Projeto Final Bloco 03

Aplicação web desenvolvida em **React + TypeScript** para gerenciamento de produtos farmacêuticos, consumindo uma API REST própria. O sistema permite visualizar, cadastrar, editar e excluir produtos e seus relacionamentos de categoria.

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

Representa um item do estoque da farmácia.

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

### Categoria (Relacionamento)

Agrupa os produtos por tipo ou finalidade.

```ts
interface Categoria {
  id: number;
  tipo: string;
  descricao: string;
  produto?: Produto[];
}
```

> Uma **Categoria** pode conter vários **Produtos** (relacionamento 1:N).

---

## ⚙️ Como Rodar o Projeto

### Pré-requisitos

- Node.js 18+
- npm ou yarn
- API backend rodando localmente

### Instalação

```bash
# Clone o repositório
git clone https://github.com/clarodriguess/projeto_final_bloco_03.git

# Entre na pasta
cd projeto_final_bloco_03

# Instale as dependências
npm install
```

### Configuração da API

Certifique-se de que a sua API está rodando. Por padrão, o Axios aponta para:

```
http://localhost:8080
```

Se necessário, ajuste a `baseURL` no arquivo de configuração do Axios em `src/services/`.

### Executar em desenvolvimento

```bash
npm run dev
```

Acesse em: [http://localhost:5173](http://localhost:5173)

### Build para produção

```bash
npm run build
```

---

## 🔗 Endpoints Consumidos

| Método | Endpoint | Descrição |
|---|---|---|
| GET | `/produtos` | Lista todos os produtos |
| GET | `/produtos/:id` | Busca produto por ID |
| POST | `/produtos` | Cadastra novo produto |
| PUT | `/produtos` | Atualiza produto |
| DELETE | `/produtos/:id` | Remove produto |
| GET | `/categorias` | Lista todas as categorias |
| GET | `/categorias/:id` | Busca categoria por ID |
| POST | `/categorias` | Cadastra nova categoria |
| PUT | `/categorias` | Atualiza categoria |
| DELETE | `/categorias/:id` | Remove categoria |

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

Desenvolvido por **Clarisse Rodrigues** como projeto final do Bloco 03.

[![GitHub](https://img.shields.io/badge/GitHub-clarodriguess-181717?style=flat&logo=github)](https://github.com/clarodriguess)