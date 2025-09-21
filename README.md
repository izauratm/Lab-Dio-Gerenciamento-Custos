# 🏦 Resumo do Lab: Gerenciamento de Custos no Microsoft Azure AZ-900
Este repositório reúne os principais aprendizados adquiridos durante o curso **Gerenciamento de Custos no Azure** da plataforma [DIO.me](https://web.dio.me), Gerenciamento e Governança na Azure - Módulo 3. O foco está nos benefícios e aplicações práticas da plataforma Microsoft Azure, explorando seus recursos e funcionalidades.
O Bootcamp oferece uma base sólida em tecnologias de nuvem, abordando desde os conceitos fundamentais até os componentes essenciais da arquitetura Azure. Entre os temas estudados estão: criação e gerenciamento de máquinas virtuais, configuração de bancos de dados e soluções de armazenamento, além de tópicos avançados como arquitetura em nuvem, governança, monitoramento e segurança de ambientes cloud. 

---

## 📘 Tópicos Abordados

Este repositório apresenta um resumo sobre como gerenciar os custos na Azure. Gerenciar os custos é uma prática essencial para otimizar seus gastos e garantir que estamos usando os recursos de forma eficiente. 
O serviço Azure Cost Management and Billing é a principal ferramenta para acompanhar e controlar esses custos.

---

## 📝 Fatores que Afetam os Custos

O custo de usar os serviços da Azure pode variar com base em diversos fatores. Entender esses elementos é o primeiro passo para um gerenciamento de custos eficaz.
- **Tipo de serviço:** O custo difere entre os serviços, como máquinas virtuais (VMs), armazenamento, bancos de dados e serviços de rede
- **Localização geográfica:** Os preços podem variar dependendo da região onde seus recursos estão hospedados devido a custos de energia e mercado local. Regiões diferentes têm preços distintos.
- **Modelo de cobrança:** Pay-as-you-go, reservas, instâncias spot.
- **Escalabilidade:** Recursos que escalam automaticamente podem gerar custos variáveis.
- **Licenciamento:** Softwares com licenças adicionais (ex: Windows Server).
- **Volume de Uso:** A quantidade de dados processados, o número de transações e a duração do tempo de execução dos recursos influenciam diretamente no custo.
- **Nível de Serviço (SKU):** A maioria dos serviços oferece diferentes "SKUs" (Stock Keeping Units) com funcionalidades e preços distintos. Por exemplo, uma VM pode ter tamanhos e séries variados.
- **Transferência de Dados:** O tráfego de dados de saída (da Azure para a internet ou entre regiões) geralmente é cobrado.


## 🛒 Azure Marketplace
O Azure Marketplace é uma loja online que oferece milhares de soluções e serviços de terceiros e da Microsoft, que são integrados à sua fatura do Azure.
Os custos desses serviços são adicionados à sua fatura e variam conforme o fornecedor e o modelo de cobrança.
- **Como Funciona:** Você pode encontrar imagens de VMs, aplicações de software, serviços de consultoria e mais. Os custos desses produtos são adicionados à sua fatura mensal do Azure.
- **Modelos de Cobrança:** Os preços podem ser baseados em uso (pago por hora/mês), taxa fixa ou planos de assinatura. É crucial verificar a página de cada produto para entender seu modelo de preços.

## 🧮 Calculando o Custo Total na Azure 
A melhor ferramenta para estimar seus gastos é a Calculadora de Preços da Azure.
* **1. Acesse a Calculadora:** Utilize a ferramenta oficial da Microsoft para simular os custos de sua arquitetura.
* **2. Adicione e Configure:** Selecione os serviços que você planeja usar (VMs, banco de dados, armazenamento, etc.) e configure suas especificações, como região, tamanho e volume de dados.
* **3. Considere Descontos:** A calculadora permite que você aplique descontos de Instâncias Reservadas (RIs) e do Benefício Híbrido do Azure para obter uma estimativa mais precisa.

Use a [Calculadora de Preços da Azure](https://azure.microsoft.com/pt-br/pricing/calculator/) para estimar custos.

* **Considere:**
  * **Tempo de uso (horas/mês)**
  * **Tipo de instância**
  * **Tráfego de rede**
  * **Serviços adicionais (backup, monitoramento, etc.)**

Para um monitoramento em tempo real, use o serviço Azure **Cost Management and Billing**, que permite visualizar, analisar e gerenciar seus gastos com relatórios e alertas de gastos.
Nessas imagens visualizamos a aba (marcada em amarelo) onde podemos visualizar estratégias de melhorias de custos.

<img width="300" height="500" alt="imagem9" src="https://github.com/user-attachments/assets/792c0065-c18b-4caf-b359-9a17dee036eb"/>
<img width="600" height="400" alt="imagem10" src="https://github.com/user-attachments/assets/06b353c7-3b43-4ad3-aaf0-ea66533c9dd5"/>

### Exemplo de Cálculo para uma MV simples com o uso da Calculadora no Azure:
Valor apresentado sem nenhuma alteração, com o básico da Azure para uma MV:
<img width="500" height="500" alt="1opcao" src="https://github.com/user-attachments/assets/b260a8c8-7b7b-4f47-a176-0cc8adfabac0"/>

Valor apresentado com alteração nos dias de uso e tipo da licença - para a mesma MV!
<img width="500" height="500" alt="2opcao" src="https://github.com/user-attachments/assets/2376582c-09d9-4574-a026-3c108b6351d2"/>

**OBS:** Importante sempre simularmos várias opções de recursos e custos.

A calculadora permite que imprimamos um relatório da estimativa de gastos para melhor análise dos custos.

<img width="1345" height="681" alt="relatorio" src="https://github.com/user-attachments/assets/7ad77d30-02af-4f9c-9d2d-f09e8e4b4ff4"/>

---
## 🏷️ Marcas (Tags) no Azure
As **tags** são pares de nome-valor que ajudam a organizar e categorizar recursos e facilitar o rastreamento de custos. Elas são essenciais para um controle de custos eficaz. 
Elas funcionam como etiquetas que ajudam a identificar e agrupar recursos com base em critérios personalizados. Exemplo:
  - environment: produção
  - departamento: financeiro
  - projeto: ERP2025
<img width="500" height="440" alt="imagem8" src="https://github.com/user-attachments/assets/081d957c-f2ec-42fa-b645-374109aab4d2"/>

## 🏷️ Para que servem as Tags?

### 1. Gerenciamento de Custos
- Permite segmentar gastos por projeto, equipe ou ambiente.
- No Azure Cost Management, você pode gerar relatórios filtrando por tags.

### 2. Organização
- Facilita a busca e categorização de recursos em ambientes complexos.
- Útil em ambientes com centenas de recursos distribuídos.

### 3. Automação
- Ferramentas como Azure Policy ou scripts em PowerShell podem usar tags para aplicar regras automaticamente.

### 4. Segurança e Governança
- Tags ajudam a aplicar políticas de acesso e conformidade específicas por grupo de recursos.

---

## 🧠 Boas Práticas
- Usar nomes consistentes: evite variações como `departamento` vs `Dept`.
- Padronize valores: ex. `produção`, `desenvolvimento`, `teste`.
- Aplicar tags desde a criação do recurso (pode ser feito via portal, CLI, ARM templates ou Terraform).

---

## 📌 Como aplicar tags em recursos do Azure

### 🧭 1. Pelo Portal do Azure

**Durante a criação de um recurso:**
- Na última etapa do assistente, localize a aba chamada **"Tags"**.
- Adicione os pares de chave-valor que você deseja. Por exemplo:
  - `departamento: financeiro`
  - `ambiente: producao`
  - `projeto: ERP2025`
- Prossiga para a revisão e criação do recurso.

**Após a criação:**
- Acesse o recurso.
- Vá até a aba **"Tags"** no menu lateral.
- Clique em **"Adicionar"** ou **"Editar"** e salve.

## ✅ Conclusão
O gerenciamento de custos na Azure é muito mais do que apenas economizar dinheiro; é uma prática de governança essencial que garante o uso eficiente e estratégico dos recursos de nuvem. Ao integrar ferramentas como o Azure Cost Management and Billing, a Calculadora de Preços e a utilização estratégica de tags, as empresas transformam gastos de nuvem de uma despesa incontrolável em um investimento planejado e previsível.

> Este conteúdo faz parte do projeto **Otimizando Custos no Azure - Laboratório** da plataforma DIO.me.

---
 
### 📚 Recursos Complementares
- [Tutorial oficial para criar e gerenciar VMs Windows](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/tutorial-manage-vm)
- [SQL do Azure para Iniciantes](https://learn.microsoft.com/pt-br/shows/azure-sql-for-beginners/)
- [Portal Microsoft Azure](https://portal.azure.com/#allservices)
- [Calculadora de Preços Azure](https://azure.microsoft.com/pt-br/pricing/calculator/)
- [Como usar as Tags para organizar recursos](https://learn.microsoft.com/pt-br/azure/azure-resource-manager/management/tag-resources)
  
📎 Link do curso: [Microsoft Azure AZ-900 - DIO.me](https://web.dio.me/track/microsoft-azure-az-900)

🖼️ Imagens: Fonte Dio.me e Calculadora de Preço Azure






