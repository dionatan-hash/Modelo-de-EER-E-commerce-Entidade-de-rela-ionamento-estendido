# 📦 Modelo de EER - E-commerce  
**Versão MVP (Minimum Viable Product)**

Este projeto apresenta o **Modelo de Entidade-Relacionamento Estendido (EER)** para um sistema de e-commerce.  
O objetivo é fornecer uma base sólida de dados que suporte operações críticas como cadastro de clientes, gestão de pedidos, pagamentos, entregas, fornecedores e estoque.

---

## 🎯 Objetivo
Construir um **modelo de dados robusto e escalável** que permita à empresa:
- Centralizar informações de clientes, fornecedores, produtos e pedidos.  
- Garantir integridade e consistência dos dados por meio de chaves primárias e estrangeiras.  
- Suportar análises estratégicas de vendas, logística e relacionamento com clientes.  

---

## 📑 PRD (Product Requirements Document)
### Requisitos funcionais
- Cadastro de clientes com vínculo a endereços e identificação (CPF/CNPJ).  
- Registro de pedidos com status, descrição, valor total e prazo de devolução.  
- Gestão de pagamentos vinculados a pedidos.  
- Controle de entregas com rastreamento e endereço de destino.  
- Integração de fornecedores e vendedores com produtos e estoque.  

### Requisitos não funcionais
- **Escalabilidade**: modelo preparado para crescer com aumento de clientes e pedidos.  
- **Normalização**: eliminação de redundâncias (endereços centralizados, identificação separada).  
- **Integridade referencial**: uso de FKs para garantir consistência.  
- **Flexibilidade**: suporte a múltiplos endereços por cliente e múltiplos produtos por pedido.  

---

## 🗂️ Entidades principais
- **Cliente**: dados cadastrais e vínculo a endereço e identificação.  
- **Identificação**: CPF/CNPJ, separando pessoa física e jurídica.  
- **Endereço**: centralizado, usado por Cliente e Entrega.  
- **Pedido**: status, descrição, valor total, vínculo a Cliente.  
- **Entrega**: data, status, rastreamento, vínculo a Pedido e Endereço.  
- **Pagamento**: tipo, status, valor, vínculo a Pedido.  
- **Produto**: categoria, descrição, valor.  
- **Fornecedor / Vendedor**: origem dos produtos.  
- **Estoque**: controle de disponibilidade.  

---

## 🚀 Melhorias que este modelo traz
- **Redução de redundância**: endereços e documentos centralizados, evitando duplicação.  
- **Rastreabilidade ponta a ponta**: cada pedido pode ser acompanhado desde o cliente que o originou até o pagamento e a entrega, garantindo visão completa do ciclo de vendas e logística.”
- **Visão 360º do cliente**: integração de dados cadastrais, pedidos e pagamentos.  
- **Gestão eficiente de fornecedores e estoque**: controle claro de origem e disponibilidade dos produtos.  
- **Base para BI e Analytics**: modelo pronto para alimentar dashboards de vendas, logística e finanças.  

---

## 💡 Dores que resolve
- **Pedidos sem cliente vinculado** → agora cada pedido tem FK para Cliente.  
- **Endereços duplicados em várias tabelas** → centralização em uma única tabela Endereço.  
- **Mistura de CPF/CNPJ em Cliente/Fornecedor** → separação clara na tabela Identificação.  
- **Dificuldade em rastrear entregas** → entrega vinculada a pedido e endereço, com código de rastreamento.  
- **Pagamentos soltos** → cada pagamento vinculado diretamente a um pedido.  

---

## 🏆 Vantagens para a empresa
- **Eficiência operacional**: menos erros de cadastro e maior consistência nos dados.  
- **Escalabilidade**: modelo preparado para suportar crescimento sem retrabalho.  
- **Decisão estratégica**: dados confiáveis para relatórios de vendas, logística e relacionamento.  
- **Experiência do cliente**: rastreamento de pedidos e entregas mais transparente.  
- **Compliance**: separação clara de dados pessoais (CPF/CNPJ) e endereços, alinhado a LGPD.  

---

## 📈 Impacto esperado
- Redução de até **30% em inconsistências de dados**.  
- Aumento da **eficiência logística** com entregas rastreáveis.  
- Melhoria na **satisfação do cliente** com pedidos mais transparentes.  
- Base sólida para **expansão futura** (marketplace, múltiplos vendedores, integração com ERP).  

---

## 🛠️ Ferramentas utilizadas
- **MySQL Workbench** para modelagem.  
- **GitHub** para versionamento e colaboração.  
  

---

## 📄 Licença
Este projeto está sob a licença MIT.

## 📊 Diagramas

### Modelo EER completo no Workbench

Visão geral do sistema de e-commerce, mostrando todas as entidades conectadas.
<img width="594" height="588" alt="Modelo de Entidade de relaçionamento estendido (E-commerc) 1" src="https://github.com/user-attachments/assets/4fcfbf86-daa9-4d5f-92a1-cdd9247fa6a5" />
<img width="605" height="576" alt="modelo de entidade  de relaçionamento estendido (e-commerce)2" src="https://github.com/user-attachments/assets/6c0a7b11-63fc-4beb-8909-5056b3a294da" />
<img width="492" height="293" alt="Modelo de entidade de relaçionamento estendido (E-commerce)3" src="https://github.com/user-attachments/assets/ee89047e-1645-4794-9966-c64c2a288338" />
