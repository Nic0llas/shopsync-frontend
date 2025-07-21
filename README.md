# ShopSync Sistema (Frontend)

Sistema de gestão de estoque, vendas, clientes e relatórios, com interface moderna e responsiva, desenvolvido em **React + TypeScript**, utilizando **Vite** para performance e **Tailwind CSS** para o design.

> ⚠️ Este projeto ainda está em fase de desenvolvimento — melhorias visuais, correções de usabilidade e novas funcionalidades estão sendo implementadas continuamente.

---

## 🚀 Funcionalidades Principais

- **Home**: Visão geral de produtos, vendas, clientes e pedidos pendentes.
- **Gestão de Produtos**: Cadastro, edição, exclusão e listagem com controle de estoque e categorias.
- **Gestão de Vendas**: Registro, visualização e cancelamento de vendas, com relatórios detalhados.
- **Gestão de Clientes e Fornecedores**: Cadastro, edição, exclusão e buscas.
- **Gestão de Categorias**: Organização e filtragem de produtos por categoria.
- **Relatórios**: Exportação em CSV de vendas e produtos.
- **Ações Rápidas**: Acesso rápido a funções frequentes.
- **Chatbot (beta)**: Assistente virtual integrado (em fase de testes).
- **Autenticação**: Login, registro, recuperação de senha e rotas protegidas.
- **Tema Claro/Escuro**: Alternância de tema com persistência.

---

## 🛠️ Tecnologias Utilizadas

- [React 18](https://react.dev/)
- [TypeScript](https://www.typescriptlang.org/)
- [Vite](https://vitejs.dev/)
- [Tailwind CSS](https://tailwindcss.com/)
- [React Router DOM](https://reactrouter.com/)
- [Axios](https://axios-http.com/)
- [Lucide React](https://lucide.dev/)
- [Headless UI](https://headlessui.dev/)
- [Docker](https://www.docker.com/) + [Docker Compose](https://docs.docker.com/compose/)

---

## 📁 Estrutura de Pastas
```
├── src/
│ ├── components/ # Componentes reutilizáveis (Sidebar, Modais, etc.)
│ ├── contexts/ # Contextos (auth, tema)
│ ├── pages/ # Páginas principais
│ ├── services/ # Conexão com API
│ ├── database/ # Mocks ou integrações locais
│ └── main.tsx # Ponto de entrada da aplicação
├── public/ # Arquivos estáticos
├── Dockerfile # Configuração para build com Nginx
├── docker-compose.yml # Orquestra frontend/backend/db
├── nginx.conf # Configuração do Nginx

```

## Instalação e Execução Local

### Pré-requisitos
- Node.js 18+
- npm ou yarn

### Passos

## 🧪 Instalação e Execução Local

### Pré-requisitos
- Node.js 18+
- npm ou yarn

### Passos

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/Nic0llas/shopsync-frontend.git
   cd shopsync-frontend

2. **Instale as dependências:**

'''
npm install

yarn install
'''

3. **Configure as variáveis de ambiente:**
   - Crie um arquivo `.env` na raiz e defina a URL da API backend:
     ```
     VITE_API_BASE_URL=http://localhost:8080

     ```
4. **Inicie o projeto em modo desenvolvimento:**
   ```bash
   npm run dev

   # ou

   yarn dev
   ```
5. **Acesse em:** [http://localhost:5173](http://localhost:5173)

## Uso com Docker

1. **Build e execução com Docker Compose:**
   ```bash
   docker-compose up --build
   ```
   - O backend e banco MySQL são orquestrados juntos (ajuste o caminho do backend no `docker-compose.yml` se necessário)

## Scripts Disponíveis

- `npm run dev` — Inicia o servidor de desenvolvimento Vite
- `npm run build` — Gera build de produção
- `npm run preview` — Visualiza build de produção localmente
- `npm run lint` — Lint do código com ESLint

## Autenticação e Segurança
- JWT armazenado no localStorage
- Refresh automático de token
- Rotas protegidas por contexto e componente `ProtectedRoute`

## Temas
- Suporte a tema claro/escuro com persistência no localStorage

## Customização
- Edite os componentes em `src/components/` para personalizar a interface
- Adicione novas páginas em `src/pages/`
- Ajuste variáveis de ambiente conforme necessário

## Licença
Este projeto é open-source sob a licença MIT.