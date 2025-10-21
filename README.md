<div align="center">

| <img src="./frontend/public/placeholder.svg" width="80" alt="BioAccess Icon" align="center"> | <h1 align="center">Biometric Access System</h1> |
|----------------------------------------------------------------------------|:---------------------------------:|

---

</div>

<div>
<img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white">
<img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=black">
<img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black">
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white">
<img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white">
<img src="https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">
<img src="https://img.shields.io/badge/Fastify-%23000000.svg?style=for-the-badge&logo=fastify&logoColor=white">
<img src="https://img.shields.io/badge/Prisma-%2314BF96.svg?style=for-the-badge&logo=Prisma&logoColor=white">
<img src="https://img.shields.io/badge/Zod-%233068b7.svg?style=for-the-badge&logo=zod&logoColor=white">
<img src="https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens">
<img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white">
<img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white">
</div>

---

## 💻 Nome do Projeto
**Biometric Access System**

## 🏫 Instituição
ETEC Dr. Geraldo José Rodrigues Alckmin - Taubaté

## 👥 Integrantes da Equipe
- Arthur Roberto Weege Pontes (Backend TypeScript e Frontend React)
- Douglas Henrique Santos Xavier & Guilherme Moreira da Rocha (Sistema Python)
- Guilherme Silveira Fernandes (Interface C++)

## 📋 Descrição do Projeto
O **Biometric Access System** é um sistema completo de controle de acesso biométrico desenvolvido para instituições de ensino. Ele integra diversas tecnologias para o cadastro, verificação e gerenciamento de biometrias, utilizando o sensor R307. A solução oferece uma interface web intuitiva para administração e módulos de backend para processamento de dados e comunicação com hardware.

> Trabalho de Conclusão de Curso (TCC) - ETEC Dr. Geraldo José Rodrigues Alckmin

---

## 🗺️ Estrutura do Projeto

O projeto está organizado em módulos de tecnologia, facilitando o desenvolvimento e a manutenção:

| Diretório | Tecnologia | Descrição | README Específico |
| :--- | :--- | :--- | :--- |
| **`backend/`** | TypeScript/Node.js | Contém a API RESTful, lógica de negócios e comunicação com o banco de dados via Prisma ORM. | [backend/README.md](./backend/README.md) |
| **`frontend/`** | React/TypeScript | Interface de usuário (Web App) para administração e visualização de logs. | [frontend/README.md](./frontend/README.md) |
| **`python/`** | Python | Módulo responsável pela consulta e comunicação com o sensor biométrico (R307) e registro de acesso. | [python/README.md](./python/README.md) |
| **`c++/`** | C++ | Interface de comunicação de baixo nível ou módulo de integração de hardware. | [c++/README.md](./c++/README.md) |

---

## 🎥 Vídeo Sobre o Projeto

*   **A ser adicionado:** Link para vídeo de demonstração do projeto.

---

## 🛠️ Tecnologias Utilizadas

### Backend TypeScript
- **Linguagem:** Node.js (TypeScript)
- **Framework:** Fastify
- **Banco de Dados:** PostgreSQL
- **ORM:** Prisma
- **Validações:** Zod
- **Autenticação:** JWT
- **Criptografia:** bcrypt

### Sistema Python
- **Linguagem:** Python
- **Conexão DB:** psycopg2
- **Comunicação Serial:** pyserial (para sensor)
- **Codificação:** base64
- **Logs:** logging

### Frontend React
- **Framework:** React
- **Build Tool:** Vite
- **Estilização:** Tailwind CSS
- **UI Library:** shadcn/ui
- **Roteamento:** React Router
- **Ícones:** Lucide Icons

### Interface C++
- **Comunicação Serial:** Para sensor R307
- **Comunicação HTTP:** Para interagir com o Backend TypeScript
- **Comunicação Interprocessos (IPC) / Socket:** Para interagir com o Sistema Python

---

## ⚙️ Instruções de Setup

### Requisitos
- **Node.js**: versão `18+`
- **Python**: versão `3.11+`
- **PostgreSQL**
- **Sensor R307** (para produção e testes físicos)

### 1. Clonar repositório
```bash
git clone https://github.com/TCCpanthers/biometricaccesssystem.git
cd biometricaccesssystem
```

### 2. Configurar e Iniciar Backend TypeScript (API)

**Instalação e Configuração:**
```bash
cd backend
npm install
# Configure seu .env (copie de .env-example)
npx prisma generate
npx prisma db push
```
**Execução:**
```bash
npm run dev
```
Servidor disponível em `http://localhost:3333` (porta padrão, pode ser alterada no `.env`).

### 3. Sistema Python (Consulta Biométrica)
```bash
cd python
pip install -r requirements.txt

# Configurar variáveis de ambiente
cp .env.example .env
# Editar .env com suas configurações de banco de dados e sensor

# Executar em modo simulação (para testes sem sensor real)
python main.py --mode simulation --unit ETEC01

# Executar em modo produção (com sensor R307 real)
python main.py --mode listener --unit ETEC01
```

### 4. Frontend React (TSX)
```bash
cd frontend
npm install
npm run dev
```
Interface disponível em `http://localhost:5173` (ou porta configurada no `.env`)

### 5. Interface C++
```bash
cd c++
# Siga as instruções específicas no README.md deste módulo para compilação e execução.
```

---

## 🌐 Variáveis de Ambiente

As variáveis de ambiente são específicas para cada módulo. Consulte os arquivos `.env-example` em cada diretório de tecnologia para detalhes.

| Módulo | Arquivo de Configuração |
| :--- | :--- |
| **Backend** | `backend/.env` |
| **Python** | `python/.env` |
| **Frontend** | `frontend/.env` |

---

## 📄 Documentação da API

A documentação interativa da API (Swagger UI) pode ser acessada ao iniciar o servidor TypeScript, visitando a rota `/docs` em seu navegador:

`http://localhost:3333/docs` (porta padrão)

Você pode importar as rotas para o seu cliente API (como Insomnia ou Postman) utilizando o arquivo:

- <u><a href="./backend/insomnia.json">Rotas API em arquivo .json</a></u>

---

## 🚨 Troubleshooting

Para solução de problemas, consulte o **README.md** de cada módulo ou a seção de Troubleshooting no [README.md do Backend](./backend/README.md).

---

## ❓ Perguntas Frequentes

**Q: Como testar o sistema sem um dispositivo biométrico físico?**
R: Utilize o modo de simulação do sistema Python. No diretório `python`, execute: `python main.py --mode simulation --unit ETEC01`

**Q: Como resetar o banco de dados e aplicar novas migrações?**
R: No diretório `backend`, execute: `npx prisma migrate reset`

**Q: Onde posso encontrar mais detalhes técnicos sobre a arquitetura e implementação?**
R: Consulte os arquivos `README.md` específicos de cada módulo (`frontend`, `python`, `c++`) e a documentação gerada pelo Swagger UI (`/docs`).

---

> Desenvolvido com 😡 para o TCC do curso de Análise e Desenvolvimento de Sistemas  
> ETEC Dr. Geraldo José Rodrigues Alckmin - 2025  
> Contato: tccpanthersoficial@gmail.com

