# **Infraestrutura em Nuvem: IaaS, PaaS, SaaS e Criação de Instâncias no Azure**

Este repositório contém informações e exemplos sobre os modelos de serviços de nuvem **IaaS**, **PaaS** e **SaaS**, bem como um guia para criar uma instância no **Azure**, incluindo detalhes sobre Zonas de Disponibilidade (AZ) e a arquitetura da nuvem.

## **Índice**

- [IaaS, PaaS e SaaS](#iaas-paas-e-saas)
  - [IaaS (Infraestrutura como Serviço)](#iaas)
  - [PaaS (Plataforma como Serviço)](#paas)
  - [SaaS (Software como Serviço)](#saas)
- [Como Criar uma Instância no Azure](#como-criar-uma-instancia-no-azure)
  - [O que são Zonas de Disponibilidade (AZ)](#o-que-são-zonas-de-disponibilidade-az)
  - [Passo a Passo para Criar uma Instância no Azure](#passo-a-passo-para-criar-uma-instancia-no-azure)

---

## **IaaS, PaaS e SaaS**

### **IaaS (Infraestrutura como Serviço)**

**IaaS** é um modelo de serviço em que a infraestrutura básica necessária para rodar aplicações é fornecida pelo provedor de nuvem. Isso inclui servidores, redes, armazenamento e outras tecnologias essenciais. O usuário tem controle sobre o sistema operacional e as aplicações que são instaladas, mas não sobre o hardware subjacente.

**Exemplos de IaaS:**
- **Microsoft Azure:** Virtual Machines, Virtual Networks, etc.
- **Amazon Web Services (AWS):** EC2, S3, etc.
- **Google Cloud Platform (GCP):** Compute Engine, Cloud Storage, etc.

### **PaaS (Plataforma como Serviço)**

**PaaS** oferece uma plataforma que inclui infraestrutura, sistema operacional, servidores, rede, armazenamento, além de ferramentas para o desenvolvimento de software. O usuário não precisa gerenciar a infraestrutura subjacente, mas pode focar no desenvolvimento das aplicações.

**Exemplos de PaaS:**
- **Microsoft Azure:** Azure App Services, Azure SQL Database, etc.
- **Google Cloud Platform (GCP):** App Engine, Cloud Functions, etc.
- **Heroku:** Um exemplo de plataforma PaaS focada em desenvolvedores.

### **SaaS (Software como Serviço)**

**SaaS** é um modelo em que o software está disponível na nuvem e acessado via internet. O provedor de nuvem gerencia toda a infraestrutura e manutenção, enquanto o usuário final apenas utiliza o software sem se preocupar com os detalhes técnicos.

**Exemplos de SaaS:**
- **Google Workspace:** Gmail, Google Drive, Google Docs, etc.
- **Microsoft 365:** Word Online, Excel Online, etc.
- **Salesforce:** CRM na nuvem.

---

## **Como Criar uma Instância no Azure**

Abaixo está um passo a passo de como criar uma instância (máquina virtual) no Microsoft Azure. Para esse processo, vamos utilizar a **Azure Portal**, mas você também pode utilizar o **Azure CLI** ou **ARM Templates**.

### **O que são Zonas de Disponibilidade (AZ)?**

No Azure, uma **Zona de Disponibilidade** (AZ) é uma divisão de data centers em uma região. Cada AZ é composta por um ou mais data centers fisicamente isolados, mas interconectados. Isso significa que se um data center em uma AZ falhar, as outras AZs continuam operando, garantindo alta disponibilidade e tolerância a falhas.

- **Cada AZ** tem sua própria energia, refrigeração e rede.
- **Regiões** do Azure são compostas por uma ou mais AZs.
- Utilizar múltiplas AZs pode melhorar a disponibilidade e resiliência da sua aplicação.

### **Passo a Passo para Criar uma Instância no Azure**

1. **Acessar o Azure Portal:**
   - Acesse o [Azure Portal](https://portal.azure.com/).

2. **Criar um Novo Recurso:**
   - Clique em "Criar um recurso" no painel inicial.

3. **Escolher a Máquina Virtual:**
   - Na barra de pesquisa, digite "Máquina Virtual" e clique na opção correspondente.

4. **Configuração da Máquina Virtual:**
   - **Assinatura:** Selecione sua assinatura.
   - **Grupo de Recursos:** Selecione um grupo de recursos existente ou crie um novo.
   - **Nome:** Defina um nome para a sua máquina virtual.
   - **Região:** Selecione a região onde deseja hospedar a máquina. Preste atenção ao selecionar uma região que tenha múltiplas **Zonas de Disponibilidade** para garantir alta disponibilidade (por exemplo, **Brasil Sul**, **Leste dos EUA**, etc.).
   - **Imagem:** Selecione o sistema operacional que deseja utilizar (Windows, Linux, etc.).
   - **Tamanho:** Escolha o tamanho da máquina virtual com base nas suas necessidades (quantidade de CPU, RAM, etc.).

5. **Configurações de Rede:**
   - Escolha ou crie uma rede virtual (VNet) e configure sub-redes.
   - Selecione a opção de Zonas de Disponibilidade: você pode escolher uma AZ específica ou permitir que o Azure aloque automaticamente a máquina em uma zona.

6. **Configuração de Discos:**
   - Defina o disco de inicialização (geralmente SSD ou HDD).
   - Caso necessário, adicione discos adicionais.

7. **Configuração de Segurança:**
   - Defina as configurações de segurança, como firewall, grupo de segurança de rede (NSG), e chaves SSH ou senhas.

8. **Revisar e Criar:**
   - Revise as configurações e clique em "Criar" para iniciar a criação da sua instância.

---

## **Conclusão**

Agora você já sabe a diferença entre os modelos IaaS, PaaS e SaaS, e como criar uma instância no Azure utilizando Zonas de Disponibilidade para garantir alta disponibilidade e resiliência. A nuvem oferece flexibilidade e escalabilidade para soluções de TI, e o Azure fornece uma plataforma robusta para atender às necessidades de diferentes tipos de aplicativos e cargas de trabalho.

---

## **Links Úteis**

- [Documentação oficial do Azure](https://learn.microsoft.com/pt-br/azure/)
- [Criar uma máquina virtual no Azure](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal)
- [Mais sobre Zonas de Disponibilidade no Azure](https://learn.microsoft.com/pt-br/azure/availability-zones/az-overview)
