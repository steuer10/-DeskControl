# 🖥️ DeskControl

> Plataforma web para auxiliar profissionais analistas de Control Desk no gerenciamento de chamados, monitoramento de infraestrutura e controle de SLA.

---

## 📋 Descrição do Projeto

Analistas de Control Desk enfrentam diariamente o desafio de gerenciar múltiplos chamados simultâneos, monitorar a infraestrutura de TI e garantir o cumprimento de SLAs — muitas vezes utilizando ferramentas dispersas e pouco integradas.

**DeskControl** centraliza todas essas operações em uma única plataforma web, aumentando a produtividade do analista e a qualidade do atendimento prestado.

---

## 🎯 Funcionalidades

### Requisitos Funcionais (RF)
- ✅ Cadastro e autenticação de usuário (login/registro com perfis: analista e admin)
- ✅ Abertura, acompanhamento e encerramento de chamados/tickets
- ✅ Classificação de chamados por prioridade (baixa, média, alta, crítica)
- ✅ Painel de monitoramento de infraestrutura em tempo real (status de serviços)
- ✅ Controle de SLA com alertas de prazo e relatórios de cumprimento
- ✅ Histórico completo de chamados por analista
- ✅ Dashboard com indicadores de desempenho (KPIs)
- ✅ Geração de relatórios exportáveis (PDF/CSV)

### Requisitos Não Funcionais (RNF)
- Interface responsiva e intuitiva para uso em múltiplos monitores
- Autenticação segura com JWT e controle de perfis
- Notificações em tempo real para chamados críticos
- Dados persistidos em banco relacional
- Tempo de resposta inferior a 2 segundos nas consultas

---

## 🛠️ Tecnologias

| Tecnologia | Função | Justificativa |
|---|---|---|
| **React** | Frontend | SPA dinâmica, ideal para dashboards em tempo real |
| **Node.js + Express** | Backend | Leve, rápido e mesma linguagem do frontend |
| **PostgreSQL** | Banco de dados | Robusto para dados relacionais complexos (tickets, SLA, usuários) |
| **Prisma ORM** | Acesso ao banco | Facilita queries e migrações de forma segura |
| **Socket.io** | Tempo real | Notificações instantâneas para chamados críticos |
| **JWT** | Autenticação | Stateless, seguro e simples de implementar |
| **Chart.js** | Gráficos | Visualização de KPIs e relatórios no dashboard |
| **Render / Railway** | Deploy | Gratuito e prático para MVP |

---

## 🗂️ Organização de Tarefas

| Semana | Foco |
|---|---|
| 1 | Modelagem do banco, rotas backend, autenticação e perfis |
| 2 | CRUD de chamados, classificação por prioridade e SLA |
| 3 | Painel de monitoramento, notificações em tempo real |
| 4 | Dashboard com KPIs, relatórios e integração front/back |
| 5 | Testes, ajustes finais e deploy |

---

## 🗃️ Modelagem de Dados (Resumo)

```
Usuario         Chamado           SLA
--------        --------          --------
id              id                id
nome            titulo            chamado_id
email           descricao         prazo_horas
senha           prioridade        status
perfil          status            cumprido
                analista_id       
                criado_em         
                encerrado_em      
```

---

## 🚀 Como Executar

### Pré-requisitos
- Node.js 18+
- PostgreSQL

### Backend
```bash
cd backend
npm install
npx prisma migrate dev
npm run dev
```

### Frontend
```bash
cd frontend
npm install
npm run dev
```

### Variáveis de Ambiente (.env)
```env
DATABASE_URL="postgresql://usuario:senha@localhost:5432/deskcontrol"
JWT_SECRET="sua_chave_secreta"
PORT=3333
```

---

## 📊 Indicadores do Dashboard (KPIs)

- Total de chamados abertos / encerrados
- Taxa de cumprimento de SLA (%)
- Tempo médio de resolução por analista
- Chamados por prioridade
- Disponibilidade dos serviços monitorados

---

## 👤 Autor

Desenvolvido por **[Seu Nome]**  
Disciplina: Engenharia de Software  

---

## 📄 Licença

Este projeto está sob a licença MIT.
