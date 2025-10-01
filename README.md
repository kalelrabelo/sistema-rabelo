# 💎 Sistema ERP Joalheria Antonio Rabelo

## 📋 Visão Geral
Sistema completo de gestão para joalheria com funcionalidades de catálogo, vendas, estoque e controle financeiro.

## 🚀 Status do Projeto
- **Versão**: 2.2.0
- **Status**: ✅ Pronto para Produção
- **Última Atualização**: 22/09/2025

## ✨ Funcionalidades Principais

### ✅ Funcionalidades Implementadas
- **Catálogo de Joias** com 850+ imagens mapeadas corretamente
- **Sistema de Login** com autenticação JWT
- **Gestão de Clientes** com CRUD completo
- **Controle de Estoque** com alertas de quantidade
- **Sistema de Vendas** com carrinho e checkout
- **Gestão Financeira** com relatórios
- **Painel Administrativo** com dashboard
- **Interface Responsiva** estilo Netflix

### 🔧 Correções Recentes (v2.2.0)
- ✅ Mapeamento correto das imagens do catálogo (`/images/jewelry/`)
- ✅ Script `iniciar_windows.bat` otimizado para Windows
- ✅ Limpeza de arquivos de versões antigas
- ✅ Organização da estrutura de pastas

## 🖥️ Tecnologias Utilizadas

### Backend
- Python 3.8+
- Flask 2.0
- SQLAlchemy
- JWT Authentication
- Flask-CORS

### Frontend
- React 18
- Vite
- TailwindCSS
- Lucide Icons
- Axios

## 📦 Estrutura do Projeto
```
webapp/
├── backend/
│   ├── main.py              # Servidor Flask principal
│   ├── requirements.txt     # Dependências Python
│   ├── src/
│   │   ├── models/          # Modelos do banco de dados
│   │   ├── routes/          # Rotas da API
│   │   └── static/          # Arquivos estáticos
│   └── data/                # Banco de dados SQLite
│
├── frontend/
│   ├── src/
│   │   ├── components/      # Componentes React
│   │   ├── data/           # Dados estáticos (joiasData.js)
│   │   └── config/         # Configurações
│   ├── dist/               # Build de produção
│   │   └── images/
│   │       └── jewelry/    # 852 imagens de joias
│   └── package.json        # Dependências Node.js
│
├── iniciar_windows.bat     # Script de inicialização Windows
├── test_system.py         # Script de testes
├── ecosystem.config.cjs   # Configuração PM2
└── README.md             # Este arquivo
```

## 🚀 Como Executar

### Windows - Método Automático
```batch
# Execute o arquivo diretamente:
iniciar_windows.bat
```

### Windows - Método Manual
```batch
# Terminal 1 - Backend
cd backend
python -m venv venv
venv\Scripts\activate.bat
pip install -r requirements.txt
python main.py

# Terminal 2 - Frontend
cd frontend
npm install --legacy-peer-deps
npm run dev
```

### Linux/Mac
```bash
chmod +x start_system.sh
./start_system.sh
```

## 🌐 URLs de Acesso
- **Frontend**: http://localhost:5173
- **Backend API**: http://localhost:5000
- **Documentação API**: http://localhost:5000/api/docs

## 🔐 Credenciais de Acesso

### Administrador
- **Usuário**: admin
- **Senha**: admin123

### Funcionário
- **Usuário**: funcionario
- **Senha**: func123

## 📸 Catálogo de Joias
O sistema possui um catálogo completo com:
- **852 imagens** de alta qualidade
- **68 categorias** de joias
- Filtros por tipo, material e pedra
- Visualização detalhada com zoom
- Sistema de favoritos

## 🔍 Testes do Sistema
Execute o script de testes para verificar a integridade:
```bash
python test_system.py
```

## 📊 API Endpoints Principais

### Autenticação
- `POST /api/login` - Login de usuário
- `POST /api/register` - Registro de novo usuário

### Catálogo
- `GET /api/jewelry` - Lista todas as joias
- `GET /api/jewelry/<id>` - Detalhes de uma joia
- `GET /api/patterns` - Lista padrões de joias

### Clientes
- `GET /api/customers` - Lista clientes
- `POST /api/customers` - Adicionar cliente
- `PUT /api/customers/<id>` - Atualizar cliente
- `DELETE /api/customers/<id>` - Remover cliente

### Vendas
- `GET /api/orders` - Lista pedidos
- `POST /api/orders` - Criar pedido
- `GET /api/orders/<id>` - Detalhes do pedido

## 🛠️ Manutenção

### Backup do Banco de Dados
```bash
cd backend/data
cp joalheria.db joalheria_backup_$(date +%Y%m%d).db
```

### Atualizar Dependências
```bash
# Backend
cd backend
pip install --upgrade -r requirements.txt

# Frontend
cd frontend
npm update
```

### Limpar Arquivos Temporários
```bash
python clean_old_files.py
```

## 📝 Notas de Desenvolvimento

### Estrutura de Imagens
- Formato: `joias_<ID>_foto.png`
- Localização: `/frontend/dist/images/jewelry/`
- Total: 852 imagens mapeadas

### Configuração CORS
O backend está configurado para aceitar requisições de:
- http://localhost:5173 (desenvolvimento)
- http://localhost:5000 (produção)

## 🐛 Solução de Problemas

### Erro: "Python não encontrado"
- Instale Python 3.8+ de https://python.org
- Adicione Python ao PATH do sistema

### Erro: "Node.js não encontrado"
- Instale Node.js 16+ de https://nodejs.org
- Reinicie o terminal após instalação

### Imagens não aparecem
- Verifique se a pasta `frontend/dist/images/jewelry/` existe
- Execute `python test_system.py` para verificar

### Backend não inicia
- Verifique se a porta 5000 está livre
- Delete `backend/data/joalheria.db` se corrompido

### Frontend não compila
- Delete `frontend/node_modules` e `package-lock.json`
- Execute `npm install --legacy-peer-deps` novamente

## 📞 Suporte
Para suporte ou dúvidas sobre o sistema, consulte a documentação completa ou entre em contato com o desenvolvedor.

## 📄 Licença
Sistema proprietário - Joalheria Antonio Rabelo © 2025