# 🚀 Resumo de Aprendizado do Bootcamp Azure Essentials

Este resumo consolida o aprendizado dos laboratórios práticos do bootcamp inicial sobre a Azure, abordando conceitos essenciais para a prova AZ-900.

## 🖥️ Criando Máquinas Virtuais

Neste laboratório, aprendemos sobre os **Acordos de Nível de Serviço (SLA)**, que estabelecem os compromissos da Microsoft em relação ao tempo de atividade e conectividade de seus serviços. O SLA varia conforme a confiabilidade prometida:

| **SLA**     | **Tempo de Inatividade por Semana** | **Tempo de Inatividade por Mês** | **Tempo de Inatividade por Ano** |
|-------------|-------------------------------------|------------------------------------|------------------------------------|
| **99%**     | 1,68 hora                           | 7,2 horas                          | 3,65 dias                          |
| **99,9%**   | 10,1 minutos                        | 43,2 minutos                       | 8,76 horas                         |
| **99,95%**  | 5 minutos                           | 21,6 minutos                       | 4,38 horas                         |
| **99,99%**  | 1,01 minuto                         | 4,32 minutos                       | 52,56 minutos                      |
| **99,999%** | 6 segundos                          | 25,9 segundos                      | 5,26 minutos                       |

**🔍 Observação**: O nível de SLA pode ser afetado por como os recursos são configurados, como a implementação de redundância em contas de armazenamento, o que ajuda a garantir a disponibilidade contínua dos dados.

## ☁️ Tipos de Serviço em Nuvem

Discutimos os principais tipos de serviços em nuvem e o nível de responsabilidade compartilhada, fundamentais para entender o modelo de operações em nuvem:

### **IaaS (Infrastructure as a Service)**

IaaS fornece recursos de computação, armazenamento e rede sob demanda. Os usuários têm controle total sobre a infraestrutura, permitindo uma alta personalização. Exemplos incluem máquinas virtuais e serviços de armazenamento.

**✅ Vantagens**:
- Flexibilidade na configuração
- Pagamento por uso
- Possibilidade de escalar rapidamente

**❌ Desvantagens**:
- **Responsabilidade elevada**: O usuário deve gerenciar a segurança, backups e atualizações.
- **Complexidade**: Exige conhecimento técnico significativo para configurar e gerenciar a infraestrutura.

### **PaaS (Platform as a Service)**

PaaS oferece uma plataforma completa para desenvolver, executar e gerenciar aplicativos, sem a complexidade da infraestrutura subjacente. Ideal para desenvolvedores, este modelo permite que eles se concentrem na criação de aplicativos.

**✅ Vantagens**:
- Menos responsabilidade com a infraestrutura
- Ferramentas integradas para desenvolvimento e monitoramento
- Maior agilidade na implementação de aplicativos

**❌ Desvantagens**:
- **Menos controle**: O usuário pode ter limitações em termos de configurações e personalizações.

### **SaaS (Software as a Service)**

SaaS permite que os usuários acessem aplicativos via internet, com o provedor gerenciando toda a manutenção e atualizações. Este modelo é ideal para empresas que desejam soluções prontas para uso, minimizando a carga de TI.

**✅ Vantagens**:
- Baixa responsabilidade do cliente
- Acesso imediato a aplicações
- Atualizações automáticas

**❌ Desvantagens**:
- **Menos personalização**: Funcionalidades podem ser limitadas, dependendo do provedor.

## 🏗️ Criando Arquiteturas no Azure

Neste laboratório, exploramos as **regiões de disponibilidade** do Azure, que são centros de dados distribuídos que garantem a resiliência e a continuidade dos serviços. Aprendemos também a criar **Grupos de Recursos**, que são contêineres lógicos para gerenciar e agrupar recursos relacionados.

**🔑 Funcionalidades dos Grupos de Recursos**:
- Gerenciamento centralizado de recursos
- Aplicação de políticas e controle de acesso
- Simplificação na implementação e monitoramento

## ⚙️ Configurando Recursos em Máquinas Virtuais

Nos aprofundamos na configuração de máquinas virtuais, abordando aspectos cruciais como:

- **Região de alocação**: Local onde a VM será criada, afetando latência e conformidade.
- **Opções de disponibilidade**: Configurações que garantem a continuidade do serviço em caso de falha.
- **Configurações de disco**: Tipos de discos (HDD ou SSD) e suas respectivas performances.
- **Configurações de rede**: Como a VM se conectará à rede e quais regras de firewall aplicar.
- **Desligamento automático**: Economia de custos ao desligar VMs fora do horário de uso.
- **Opções de monitoramento**: Ferramentas para acompanhar o desempenho e saúde da VM.

## 💾 Dominando o Armazenamento na Azure

Neste laboratório, focamos na criação de **Storage Accounts** e nas opções de configuração. A **Storage Account** é fundamental para armazenar dados no Azure.

### **🛠️ Criação da Storage Account**
- **Nome único global**: O nome da conta deve ser exclusivo em toda a plataforma.
- **Região de alocação**: Local onde os dados serão armazenados, afetando latência.
- **Opção de desempenho**: Seleção entre diferentes níveis de desempenho (Standard ou Premium).
- **Níveis de redundância**:
  - **LRS (Local Redundant Storage)**: Armazenamento em múltiplas cópias em um único datacenter.
  - **ZRS (Zone Redundant Storage)**: Redundância em múltiplas zonas de disponibilidade.
  - **GRS (Geo-Redundant Storage)**: Redundância em regiões geográficas distintas.
  - **GZRS (Geo-Zone Redundant Storage)**: Combina GRS e ZRS.
- **Camadas de acesso**:
  - **Quente**: Otimizado para acesso frequente.
  - **Frio**: Ideal para dados raramente acessados, com custos menores.
- **Acesso à rede**: Configurações que controlam como os dados podem ser acessados pela rede.
- **Proteção de dados**: Opções para backup e recuperação de desastres.

### **🔍 Tipos de Armazenamento**
- **Compartilhamento de arquivos**: Acesso a arquivos de forma compartilhada via SMB.
- **Filas**: Para comunicação assíncrona entre aplicativos.
- **Tabelas**: Armazenamento de dados estruturados não-relacionais.
- **Contêineres**: Para armazenamento de blobs, como imagens e vídeos.

### **📦 Métodos de Migração**
- **Migração de servidores e bancos de dados**: Utilizando serviços dedicados como o Azure Migrate.
- **Data Box**: Dispositivos físicos para transferir grandes volumes de dados para o Azure.
  - Data Disk Box (Capaxidade máxima por pedido --> 35 TB)
  - Data Box (Capaxidade máxima por pedido --> 80 TB)
  - Data Box Heavy (Capaxidade máxima por pedido --> 800 TB)
- **AzCopy**: Ferramenta de linha de comando para copiar dados.
- **Microsoft Storage Explorer**: Interface gráfica para gerenciar e transferir dados.

## 🔒 Identidade, Acesso e Segurança na Azure

Entendemos o funcionamento do **Microsoft Entra ID**, que gerencia identidades e acessos na Azure.

### **🛠️ Abordamos**:
- **Manipulação de Usuários**:
  - **Criação de usuários**: Adição de novos usuários ao diretório.
  - **Exclusão de usuários**: Remoção de usuários que não são mais necessários.
  - **Controle de permissionamento**: Definição de papéis e permissões para acessar recursos.
  - **Redefinição de senhas**: Processo de recuperação e mudança de senhas para segurança.
- **Identidades Externas**: Integração com identidades de usuários fora da organização.
- **Microsoft Entra Connect**: Sincronização entre diretórios locais e o Azure.
- **Nomes de domínios personalizados**: Configuração de domínios que refletem a identidade organizacional.
- **Microsoft Defender for Cloud**: Proteção contra ameaças e gerenciamento de segurança em nuvem.

## 💰 Otimizando Custos na Azure

Exploramos ferramentas para estimativa de custos, fundamentais para o planejamento financeiro:

### **TCO (Total Cost of Ownership)**
A calculadora de TCO ajuda a estimar os custos associados à migração de cargas de trabalho para o Azure, permitindo uma visão clara das economias potenciais.

### **Pricing Calculator**
A calculadora de preços do Azure oferece uma maneira de transformar o uso planejado em custos estimados, facilitando o planejamento e o orçamento do uso do Azure. Permite ajustar os recursos e opções para ver como eles impactam o custo total.

## 📜 Gerenciando Políticas em Acessos Azure

Analisamos ferramentas de governança e conformidade essenciais para manter a segurança e a integridade dos dados na Azure:

### **Azure Policy**
Ajuda a impor padrões organizacionais e a avaliar a conformidade em escala. Permite criar definições de políticas que monitoram e gerenciam os recursos.

### **Bloqueio de Recursos**
Permite adicionar bloqueios de exclusão ou modificação a nível de assinatura, grupo de recursos ou recursos individuais, protegendo contra alterações acidentais.

### **Portal de Confiança do Serviço**
Oferece informações sobre implementação e segurança, auxiliando na conformidade regulatória e proteção de dados.

### **Microsoft Purview**
Conjunto de soluções para descobrir e proteger informações confidenciais, oferecendo visibilidade sobre onde os dados sensíveis estão localizados e como estão sendo usados.

## 🔧 Ferramentas de Implantação na Azure

Vimos ferramentas importantes para o gerenciamento e a implantação de recursos na Azure:

- **Portal do Azure**: Interface gráfica para gerenciamento de todos os recursos da Azure.
- **Azure Cloud Shell**: Interface baseada em navegador que permite executar comandos de linha de comando.
- **Azure PowerShell**: Conjunto de módulos do PowerShell para automação e gerenciamento.
- **CLI (Command-Line Interface)**: Interface de linha de comando para interagir com os serviços do Azure.

### **Azure Arc**
Facilita a governança e o gerenciamento ao permitir a gestão de recursos que estão fora do Azure, oferecendo uma plataforma consistente para ambientes locais e de múltiplas nuvens.

### **Azure Resource Manager (ARM)**
Serviço que permite a implantação e gestão de recursos de forma organizada e eficiente, traduzindo as requisições das ferramentas de implantação.

## 📊 Monitoramento Inteligente com o Azure

Exploramos ferramentas de monitoramento que garantem a disponibilidade e desempenho dos serviços:

### **Assistente do Azure**
Analisa recursos implantados e fornece recomendações baseadas em práticas recomendadas para otimizar a performance das implantações.

### **Integridade do Serviço do Azure**
Conjunto de serviços que mantém os usuários informados sobre o status global do Azure, incluindo a condição de serviços que podem afetar a operação.

### **Azure Monitor**
Maximiza a disponibilidade e o desempenho de aplicativos e serviços, coletando e analisando dados de telemetria de ambientes locais e na nuvem para tomar decisões informadas.

---
