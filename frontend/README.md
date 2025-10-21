<div align="center">

| <img src="./public/placeholder.svg" width="80" alt="BioAccess Frontend Icon" align="center"> | <h1 align="center">Frontend - Biometric Access System</h1> |
|----------------------------------------------------------------------------|:---------------------------------:|

---

</div>

<div>
<img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black">
<img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white">
<img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white">
<img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white">
<img src="https://img.shields.io/badge/shadcn%2Fui-000000?style=for-the-badge&logo=shadcnui&logoColor=white">
</div>

---

## 💻 Nome do Projeto
**Frontend - Biometric Access System**

## 📋 Descrição do Projeto
Este módulo é a interface de usuário do **Biometric Access System**, desenvolvido para fornecer uma experiência intuitiva e responsiva para a administração e monitoramento do sistema de controle de acesso biométrico. Ele permite o gerenciamento de biometrias, funcionários, pessoas, estudantes, professores, unidades, visitantes e visualização de logs de acesso.

---

## 🛠️ Tecnologias Utilizadas
- **Framework:** React 18
- **Linguagem:** TypeScript
- **Build Tool:** Vite
- **Estilização:** Tailwind CSS
- **UI Library:** shadcn/ui
- **Roteamento:** React Router DOM
- **Client HTTP:** Axios
- **Gerenciamento de Estado/Dados:** Tanstack Query
- **Ícones:** Lucide React

---

## ⚙️ Instruções de Setup

### Requisitos
- **Node.js**: versão `18+`
- **npm**
- **Backend do Biometric Access System** rodando (consulte o `README.md` principal para instruções)

### 1. Navegar para o diretório
```bash
cd biometricaccesssystem-project/frontend
```

### 2. Instalar dependências
```bash
npm install
```

### 3. Configurar variáveis de ambiente
Crie um arquivo `.env` na raiz desse diretório (`frontend/`) e adicione:
```env
VITE_API_URL="http://localhost:3000/api" # Ajuste para a URL do seu backend
```

### 4. Iniciar o servidor de desenvolvimento
```bash
npm run dev
```

A aplicação estará disponível em `http://localhost:5173` (ou a porta mostrada pelo Vite).

---

## 🔗 Integração com Backend

O frontend se comunica com o backend TypeScript através de requisições HTTP. A URL base da API é configurada via variável de ambiente `VITE_API_URL`.

### Autenticação
Utiliza autenticação baseada em JWT (JSON Web Tokens). Após o login, os tokens são armazenados localmente e enviados em todas as requisições autenticadas.

---

## 📱 Funcionalidades da Interface

- **Dashboard:** Visão geral do sistema.
- **Gestão de Pessoas:** CRUD para Alunos, Funcionários e Visitantes.
- **Gestão de Biometrias:** Registro e gerenciamento de digitais.
- **Logs de Acesso:** Visualização de logs biométricos e de acesso web (com filtros).
- **Gestão de Unidades:** Cadastro e gerenciamento de unidades escolares.
- **Configurações:** Opções de personalização e segurança.

### Design e Responsividade
Construído com Tailwind CSS e Shadcn/UI, garantindo um design moderno, responsivo e acessível em diferentes dispositivos.

---

## 📦 Build e Deploy

Para gerar uma versão otimizada para produção:

```bash
npm run build
```

Os arquivos estáticos gerados estarão no diretório `dist/` e podem ser servidos por qualquer servidor web estático.

---

## 🧪 Testes

Para executar os testes (se houver):

```bash
npm test
```

---

> Desenvolvido com ❤️ para o TCC do curso de Análise e Desenvolvimento de Sistemas  
> ETEC Dr. Geraldo José Rodrigues Alckmin - 2025  
> Contato: tccpanthersoficial@gmail.com

