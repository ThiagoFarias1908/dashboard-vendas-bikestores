# 📊 Dashboard Comercial - Vendas Varejo (BikeStores)

<p align="left">
  <img src="https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white" alt="SQL Server">
  <img src="https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Power BI">
  <img src="https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white" alt="DAX">
  <img src="https://img.shields.io/badge/Power_Query-742774?style=for-the-badge&logo=data&logoColor=white" alt="Power Query">
</p>

> **Status:** Concluído ✔️ <br>
> **Acesso ao Dashboard Interativo:** [Microsoft Power BI](https://app.powerbi.com/view?r=eyJrIjoiMzNmYzFiMjQtNjc3Zi00NDNlLWE1MGQtYjJlNjQ0NDkyN2E0IiwidCI6IjI3Njc2N2FmLWQ4ZjgtNDVjNC05ZGUwLWZkMWUzN2E5OGY1NiJ9) <br>
> **Estudo de Caso (Artigo detalhado):** [Leia no LinkedIn](https://www.linkedin.com/pulse/dashboard-de-vendas-thiago-farias-louren%C3%A7o-apduf/)

## 📝 1. Contexto e Problema de Negócio
A diretoria da BikeStores enfrentava gargalos operacionais devido a análises comerciais fragmentadas. O uso de controles manuais gerava lentidão nas respostas sobre a performance regional das lojas e giro de estoque por categoria, impactando o replanejamento de metas e o setor de Supply Chain. Havia a necessidade urgente de centralizar os dados transacionais em um produto analítico de alta performance.

## 🎯 2. Objetivo
Construir um Dashboard Comercial escalável de ponta a ponta, capaz de centralizar os KPIs transacionais da empresa. O objetivo principal foi entregar uma interface com alto rigor de Experiência do Usuário (UX/UI) focada em Data Storytelling, permitindo que a diretoria absorvesse métricas críticas em menos de 5 segundos.

## 🛠️ 3. Tecnologias e Ferramentas
- **Banco de Dados (Extração):** SQL Server
- **Processamento (ETL):** Power Query
- **Business Intelligence (Modelagem & DataViz):** Microsoft Power BI
- **Análise e Cálculos:** Linguagem DAX
- **Arquitetura de Dados:** Modelagem Dimensional (Star Schema e Snowflake)

## ⚙️ 4. Metodologia e Desenvolvimento Back-end

Um front-end ágil só existe com um back-end impecável. Para garantir o processamento eficiente dos registros, as seguintes técnicas de governança e modelagem de dados foram aplicadas:

- **Modelagem Dimensional:** Construção do pipeline organizando as informações em Tabelas Fato (`FactOrder`) e Dimensões descritivas (`DimCustomer`, `DimStore`).
- **Esquema Snowflake:** Implementação estratégica de hierarquias para suportar a granularidade severa entre as marcas e categorias dos produtos.
- **Time Intelligence:** Arquitetura de uma *Dimensão Calendário* otimizada, permitindo cálculos complexos de inteligência de tempo em linguagem DAX (como a Variação Anual - YoY).
- **Governança de KPIs:** Encapsulamento de todas as medidas analíticas em uma tabela dedicada, garantindo manutenibilidade e rastreabilidade para o ecossistema corporativo.

## 📈 5. Imersão Analítica (UX/UI)

Para resolver a sobrecarga cognitiva (excesso de informação) e fornecer profundidade (*drill-down*) à diretoria:
- **Custom Tooltips:** Desenvolvimento de mini-dashboards contextuais em Dicas de Ferramenta. Exemplo: Ao focar na marca "Trek", o gestor ativa um painel secundário revelando o comportamento Year-over-Year (YoY) sem sair da visão executiva principal.
- **Design Executivo:** Paleta limpa e de alto contraste focada em métricas fundamentais como Faturamento e Volume de Vendas.

## 💡 6. Principais Insights e Impacto Comercial

Ao substituir as antigas planilhas pelo modelo dimensional no Power BI, foi possível mapear padrões até então ocultos:

1. **Sazonalidade Crítica (Supply Chain):** Identificou-se que a categoria de *Mountain Bikes* concentra a maior receita em picos sazonais muito específicos. Esse insight é vital para a cadeia de suprimentos evitar rupturas de estoque.
2. **Performance Geográfica (Conversão):** O mapeamento de rentabilidade revelou forte concentração comercial na loja "Baldwin Bikes", gerando subsídios para o replanejamento estratégico e adequação de metas para filiais com menor taxa de conversão.

## 📁 7. Acesso e Arquivos do Projeto

Neste repositório, você encontrará os arquivos que atestam o back-end da solução:
*   `dash_vendas_bikestores.pbix`: O arquivo do Power BI (com os dados ofuscados/públicos).
*   `scripts_sql/`: Pasta com as *queries* utilizadas para a extração do banco de dados (ex: views criadas no SQL Server).
*   `/images`: Capturas de tela (screenshots) detalhando a interface do Dashboard e o modelo de dados gerado.

*Quando estruturamos o SQL Server, aplicamos ETL limpo e modelamos com precisão no Power BI, entregamos dados que contam histórias.*
