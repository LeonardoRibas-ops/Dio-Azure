# **Criando um Servidor de Banco de Dados SQL no Azure**

Este repositório contém informações e um passo a passo para criar um servidor de banco de dados SQL no **Azure**, com foco na criação e configuração do **Azure SQL Database**.

## **Índice**

- [O que é o Azure SQL Database](#o-que-é-o-azure-sql-database)
- [Passo a Passo para Criar um Servidor SQL no Azure](#passo-a-passo-para-criar-um-servidor-sql-no-azure)
  - [Configuração do Banco de Dados](#configuração-do-banco-de-dados)
  - [Conectar ao Banco de Dados SQL](#conectar-ao-banco-de-dados-sql)

---

## **O que é o Azure SQL Database**

O **Azure SQL Database** é um serviço de banco de dados relacional totalmente gerenciado, que oferece alta disponibilidade, segurança e escalabilidade na nuvem. Ele é baseado no **SQL Server**, mas é otimizado para a nuvem, fornecendo recursos como backup automático, patches de segurança e redundância em várias regiões.

**Principais benefícios:**
- **Escalabilidade:** Capacidade de escalar facilmente os recursos conforme necessário.
- **Alta Disponibilidade:** Disponibilidade garantida com o uso de Zonas de Disponibilidade (AZ).
- **Segurança:** Criptografia de dados em trânsito e em repouso, com recursos de segurança avançados.
- **Backup automático:** Realização de backups sem a necessidade de configuração adicional.

---

## **Passo a Passo para Criar um Servidor SQL no Azure**

Aqui está o processo para criar um servidor de banco de dados SQL no **Azure** utilizando o **Azure SQL Database**. Este passo a passo assume que você já tem uma conta no Azure.

### **1. Acessar o Azure Portal**

- Acesse o [Azure Portal](https://portal.azure.com/).

### **2. Criar um Novo Recurso**

- No painel inicial, clique em **"Criar um recurso"**.

### **3. Escolher o Serviço de Banco de Dados SQL**

- Na barra de pesquisa, digite **"SQL Database"** e clique na opção **SQL Database**.

### **4. Configuração do Banco de Dados**

- **Assinatura:** Selecione sua assinatura do Azure.
- **Grupo de Recursos:** Selecione um grupo de recursos existente ou crie um novo.
- **Nome do Banco de Dados:** Escolha um nome para o seu banco de dados.
- **Servidor:** Selecione um servidor SQL existente ou crie um novo:
  - Para criar um novo servidor, você precisará definir:
    - **Nome do servidor:** O nome do servidor SQL.
    - **Localização:** Escolha a região onde seu banco de dados será hospedado.
    - **Login do administrador:** Crie um login de administrador (nome de usuário) para o servidor.
    - **Senha:** Defina uma senha segura.
- **Modelo de Preço:** Selecione um modelo de preço com base nas suas necessidades (por exemplo, "Basic", "Standard", "Premium").

### **5. Configuração de Rede e Segurança**

- **Firewall:** Habilite ou desabilite o acesso à sua instância de banco de dados por meio de um grupo de segurança de rede.
  - Defina as regras de firewall para permitir o acesso à sua instância de banco de dados SQL de máquinas específicas ou de qualquer endereço IP.
- **Autenticação:** Verifique se a autenticação de SQL está habilitada e configure as credenciais de acesso.

### **6. Revisar e Criar**

- Após definir todas as configurações, clique em **"Revisar + Criar"**.
- Revise todas as informações e clique em **"Criar"** para iniciar a criação do servidor SQL no Azure.

### **7. Criar o Banco de Dados SQL**

- Uma vez que o servidor SQL esteja criado, você pode adicionar um banco de dados a ele.
  - Acesse o **Azure SQL Database** criado e selecione o servidor SQL.
  - Clique em **"Adicionar Banco de Dados"** e configure o banco de dados conforme necessário.

---

## **Configuração do Banco de Dados**

Após a criação do banco de dados SQL no servidor, você pode começar a configurar sua instância de banco de dados para atender às necessidades da sua aplicação. Você pode:
- Criar tabelas, índices e stored procedures.
- Definir permissões de acesso.
- Realizar backups e configurar estratégias de recuperação.

O Azure SQL Database oferece recursos como escalabilidade automática, backups automáticos, e uma variedade de opções de recuperação de desastres.

---

## **Conectar ao Banco de Dados SQL**

Agora que o servidor e o banco de dados foram criados, você pode conectar-se ao banco de dados SQL utilizando ferramentas como:

- **SQL Server Management Studio (SSMS):**
  - Abra o SSMS e insira o nome do servidor SQL, o login e a senha do administrador para se conectar ao banco de dados.
  
- **Azure Data Studio:**
  - Semelhante ao SSMS, o Azure Data Studio oferece uma interface gráfica para gerenciamento de bancos de dados SQL.

- **Conexão via Aplicações:**
  - Conecte seu banco de dados ao seu aplicativo utilizando a string de conexão do banco de dados fornecida no Azure Portal.

A string de conexão típica do Azure SQL Database se parece com:

```plaintext
Server=tcp:{nome_do_servidor}.database.windows.net,1433;Initial Catalog={nome_do_banco_de_dados};Persist Security Info=False;User ID={nome_de_usuario};Password={senha};MultipleActiveResultSets=False;Encrypt=True;TrustServerCertificate=False;Connection Timeout=30;
