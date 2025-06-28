# ServiTask - Sistema de Kanban Completo

<div align="center">

![ServiTask](https://img.shields.io/badge/ServiTask-Sistema%20de%20Kanban-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Ativo-green?style=for-the-badge)
![Version](https://img.shields.io/badge/Version-2.3-orange?style=for-the-badge)

**Sistema completo de gerenciamento de tarefas com Kanban, autenticação robusta e perfil de usuário**

[🚀 Início Rápido](#-início-rápido) • [📋 Funcionalidades](#-funcionalidades) • [🛠️ Tecnologias](#️-tecnologias) • [📚 Documentação](#-documentação)

</div>

---

## 🚀 Início Rápido

### 1. **Configurar Variáveis de Ambiente**
```bash
# Clone o repositório (se necessário)
git clone https://github.com/w1ze55/ServiTask.git
cd ServiTask

# Copie o arquivo de exemplo e configure suas credenciais
cp .env.example .env

# Edite o arquivo .env com suas credenciais seguras
# IMPORTANTE: Altere as senhas padrão por questões de segurança!
```

### 2. **Iniciar o Sistema**
```bash
cd frontend

# Faça download das dependências
npm i
cd ..

# Inicie todos os containers
docker-compose up -d --build
(necessário possuir o docker desktop instalado e rodando na sua máquina)
```

### 3. **Acessar a Aplicação**
- **🌐 Frontend**: http://localhost:3000
- **⚡ Backend API**: http://localhost:8080
- **🗄️ MySQL**: localhost:3309

### 4. **Primeiro Acesso**
1. Acesse http://localhost:3000
2. Clique em **"Criar conta"**
3. Preencha seus dados com senha segura
4. Faça login automaticamente
5. Comece a usar o sistema!

---

## 📋 Funcionalidades

### 🔐 **Autenticação e Perfil**
- ✅ **Cadastro de usuários** com validações robustas
- ✅ **Login seguro** com JWT e sessões persistentes
- ✅ **Perfil completo** com foto, nome e email
- ✅ **Upload de foto** salva no banco de dados
- ✅ **Alteração de senha** com validação da senha atual
- ✅ **Validação de senha forte** (8+ chars, maiúscula, minúscula, número, especial)
- ✅ **Mensagens de erro específicas** para cada problema

### 📊 **Sistema Kanban**
- ✅ **Quadros personalizados** para organizar projetos
- ✅ **Colunas customizáveis** (A Fazer, Em Progresso, Concluído, etc.)
- ✅ **Cards de tarefas** com título, descrição e prioridade
- ✅ **Drag & Drop** para mover cards entre colunas
- ✅ **Cores por prioridade** (Alta=vermelho, Média=amarelo, Baixa=verde)
- ✅ **CRUD completo** para quadros, colunas e cards

### 🎨 **Interface e Experiência**
- ✅ **Design moderno** com gradientes e animações
- ✅ **Responsivo** para desktop e mobile
- ✅ **Sidebar inteligente** com foto do usuário
- ✅ **Feedback visual** em tempo real
- ✅ **Temas escuros** com efeitos de blur
- ✅ **Indicadores de validação** em tempo real

### 🔒 **Segurança**
- ✅ **Autenticação JWT** com refresh automático
- ✅ **Senhas criptografadas** com BCrypt
- ✅ **Validação dupla** (frontend + backend)
- ✅ **Isolamento de dados** por usuário
- ✅ **Headers de segurança** e CORS configurado

---

## 🛠️ Tecnologias

### **Backend**
- **Java 17** - Linguagem principal
- **Spring Boot 3** - Framework principal
- **Spring Security 6** - Autenticação e autorização
- **JWT** - Tokens de acesso
- **JPA/Hibernate** - ORM para banco de dados
- **MySQL 8** - Banco de dados relacional
- **Maven** - Gerenciamento de dependências

### **Frontend**
- **React 18** - Framework JavaScript
- **Vite** - Build tool moderno
- **CSS3** - Estilização avançada com gradientes
- **Fetch API** - Comunicação com backend
- **Local Storage** - Cache de dados do usuário

### **DevOps**
- **Docker** - Containerização
- **Docker Compose** - Orquestração de containers
- **Nginx** - Servidor web para frontend
- **Multi-stage builds** - Otimização de imagens

---

## 📚 Documentação

Para informações detalhadas sobre o sistema, consulte a documentação completa na pasta `Docs/`:

### 📖 **Documentos Disponíveis**

| Documento | Descrição | Link |
|-----------|-----------|------|
| 🔄 **Fluxos e Processos** | Diagramas e fluxos de trabalho do sistema | [`Docs/FLUXOS_E_PROCESSOS.md`](./Docs/FLUXOS_E_PROCESSOS.md) |
| 📋 **Regras de Negócio** | Especificações detalhadas das funcionalidades | [`Docs/REGRAS_DE_NEGOCIO.md`](./Docs/REGRAS_DE_NEGOCIO.md) |
| 🚀 **API Documentation** | Endpoints, requests, responses e exemplos | [`Docs/API_DOCUMENTATION.md`](./Docs/API_DOCUMENTATION.md) |
| 🔐 **Validação de Senha** | Sistema completo de validação robusta de senhas | [`Docs/VALIDACAO_SENHA.md`](./Docs/VALIDACAO_SENHA.md) |

### 🎯 **Leitura Recomendada**

1. **Iniciantes**: Comece com [`REGRAS_DE_NEGOCIO.md`](./Docs/REGRAS_DE_NEGOCIO.md)
2. **Desenvolvedores**: Continue com [`API_DOCUMENTATION.md`](./Docs/API_DOCUMENTATION.md)
3. **Arquitetos**: Consulte [`FLUXOS_E_PROCESSOS.md`](./Docs/FLUXOS_E_PROCESSOS.md)

---

## 🏗️ Arquitetura

```
ServiTask/
├── 📁 backend/          # API Spring Boot
│   ├── 🔧 config/       # Configurações (Security, JWT, CORS)
│   ├── 🎮 controller/   # Endpoints REST
│   ├── 📦 service/      # Lógica de negócio
│   ├── 🗃️ repository/   # Acesso aos dados
│   ├── 🏗️ entity/       # Modelos de dados
│   └── 📋 dto/          # Objetos de transferência
├── 📁 frontend/         # Interface React
│   ├── 🎨 components/   # Componentes reutilizáveis
│   ├── 📄 pages/        # Páginas da aplicação
│   ├── 🔧 services/     # Comunicação com API
│   └── 🎭 assets/       # Recursos estáticos
├── 📁 mysql-init/       # Scripts de inicialização do DB
├── 📁 Docs/             # Documentação completa
└── 🐳 docker-compose.yml # Orquestração dos containers
```

---

## 🔧 Configuração Avançada

### **Variáveis de Ambiente**
O projeto usa arquivo `.env` para configurações sensíveis:

```bash
# Copie o arquivo de exemplo
cp .env.example .env

# Edite o .env com suas credenciais:
MYSQL_ROOT_PASSWORD=sua_senha_root_segura
MYSQL_DATABASE=servitask
MYSQL_USER=seu_usuario_mysql
MYSQL_PASSWORD=sua_senha_mysql_segura
JWT_SECRET=sua-chave-jwt-muito-segura-de-pelo-menos-32-caracteres
JWT_EXPIRATION=86400000
SPRING_PROFILES_ACTIVE=docker
```

**⚠️ IMPORTANTE**: 
- Nunca commite o arquivo `.env` no Git
- Use senhas fortes e diferentes para cada ambiente
- O arquivo `.env.example` mostra quais variáveis são necessárias

### **Comandos Úteis**
```bash
# Parar todos os containers
docker-compose down

# Reconstruir apenas o backend
docker-compose up --build backend -d

# Ver logs do backend
docker logs servitask-backend -f

# Acessar banco de dados
docker exec -it servitask-mysql mysql -u servitask -p
```

---

## 👥 Colaboradores

Este projeto foi desenvolvido em colaboração com:

- [@fshenrique6](https://github.com/fshenrique6) - Henrique Ferreira
- [@Txddyt1](https://github.com/Txddyt1) - Igor Schuller
- [@w1ze55](https://github.com/w1ze55) - Caue Peres

<div align="center">

**ServiTask** - Sistema de Kanban Completo 🚀

</div>
