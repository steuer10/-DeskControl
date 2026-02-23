# SportTrack

> Plataforma web para gerenciamento e acompanhamento de treinos esportivos pessoais.

---

## Descrição do Projeto

Atletas amadores não têm uma forma simples de registrar e acompanhar sua evolução nos treinos. Atualmente, utilizam cadernos, planilhas ou simplesmente não registram nada, perdendo histórico de desempenho e dificultando a evolução.

**SportTrack** é uma aplicação web onde o usuário cadastra seus treinos, acompanha sua evolução ao longo do tempo e visualiza seu progresso através de um dashboard interativo.

---

## Funcionalidades

### Requisitos Funcionais (RF)
- Cadastro e autenticação de usuário (login/registro)
-  Registro de treinos (data, tipo de esporte, duração, observações)
-  Listagem e histórico completo de treinos realizados
-  Dashboard com gráfico de evolução e estatísticas
-  Edição e exclusão de treinos
-  Categorização por tipo de esporte (musculação, corrida, natação, etc.)
-  Metas semanais de treino com acompanhamento de progresso

### Requisitos Não Funcionais (RNF)
- Interface responsiva e mobile-first
- Autenticação segura com JWT
- Dados persistidos em banco relacional
- Tempo de resposta inferior a 2 segundos nas consultas

---

##  Tecnologias

| Tecnologia | Função | Justificativa |
|---|---|---|
| **React** | Frontend | SPA dinâmica, componentização, grande ecossistema |
| **Node.js + Express** | Backend | Leve, rápido e mesma linguagem do frontend |
| **PostgreSQL** | Banco de dados | Confiável para dados relacionais |
| **Prisma ORM** | Acesso ao banco | Facilita queries e migrações de forma segura |
| **JWT** | Autenticação | Stateless, seguro e simples de implementar |
| **Chart.js** | Gráficos | Visualização de evolução e estatísticas no dashboard |
| **Render / Railway** | Deploy | Gratuito e prático para MVP |

---

##  Organização de Tarefas

| Semana | Foco |
|---|---|
| 1 | Modelagem do banco, rotas backend e autenticação |
| 2 | CRUD de treinos e categorização por esporte |
| 3 | Dashboard com gráficos e metas semanais |
| 4 | Integração front/back, testes e deploy |

---

## 🗃️ Modelagem de Dados (Resumo)

```
Usuario           Treino              Meta
--------          --------            --------
id                id                  id
nome              titulo              usuario_id
email             tipo_esporte        treinos_semana
senha             duracao_min         progresso
criado_em         observacoes         ativa
                  usuario_id          
                  data_treino         
```

---

##  Como Executar

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
DATABASE_URL="postgresql://usuario:senha@localhost:5432/sporttrack"
JWT_SECRET="sua_chave_secreta"
PORT=3333
```

---

##  Indicadores do Dashboard

- Total de treinos realizados no mês
- Tempo total treinado (horas)
- Esporte mais praticado
- Progresso das metas semanais (%)
- Gráfico de frequência semanal

---

##  Autor

Desenvolvido por **[VINICIUS STEUERNAGEL]**  
Disciplina: Engenharia de Software  


