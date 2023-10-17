
# Data Tranformation with Power BI 📋

[*English*] This Power BI report is a simple data visualization project focused on analyzing and presenting insights from the "Company" sample database. The focus of this analysis was on the data cleaning and transformation.

This report is a solution to the [Processando e Transformando Dados com Power BII](https://web.dio.me/project/processando-e-transformando-dados-com-power-bi/learning/a23f05bd-2d61-46b8-be0e-8d2ada4ef06a?back=/track/santander-bootcamp-2023-ciencia-de-dados-com-python&tab=undefined&moduleId=undefined) challenge proposed during the **Data Science** path of the [Santander Bootcamp](https://www.dio.me/users/nataliabrpnt)

## Table of Contents
1. [Getting started](https://github.com/nat-brpnt/desafio_transformando_dados_power_BI/edit/main/README.md#getting-started)
2. [Data Source](https://github.com/nat-brpnt/desafio_transformando_dados_power_BI/edit/main/README.md#data-source)
3. [Deliveries Checklist](https://github.com/nat-brpnt/desafio_transformando_dados_power_BI/edit/main/README.md#delieveries-checklist)


### Getting Started
To explore this Power BI report, follow these steps:

1. Prerequisites: Ensure you have Power BI Desktop installed on your machine. If not, you can download it [here](https://powerbi.microsoft.com/pt-br/downloads/).

2. Clone or Download: Clone or download this repository to your local machine.

3. Open the Report: Open the "desafio_relatorio_power_BI.pbix" file using Power BI Desktop.

4. Explore: Interact with the report, drill down into visuals, and gain insights from the financial data.

### Data Source
The report is based on the data provided by the course instructor and it can all be found [on her GitHub](https://github.com/julianazanelatto/power_bi_analyst/tree/main/M%C3%B3dulo%203/Desafio%20de%20Projeto). This database contains data of a mock up company, its employees, departments, projects and so on. The data has been preprocessed and transformed to facilitate meaningful analysis and visualization.

### Delieveries Checklist
1. Data Transformation Guidelines

2. Check column headers and data types ✅

3. Convert currency values to the double-precision data type ✅

4. Identify and handle null values ✅

5. Employees with null values in "Super_ssn" may be managers. Check for employees without managers ✅
Verify if there are any departments without managers ✅

6. If there are departments without managers, assume you have the data and fill in the gaps ✅

7. Examine project hours ✅

8. Split complex columns ✅

9. Merge employee and department queries to create an employee table with department names associated with employees. The merge should be based on the employee table. Pay attention, as this information influences the type of join ✅

10. In this process, remove unnecessary columns ✅

11. Join employees with their respective managers' names. This can be done with SQL queries or by merging tables using Power BI. If using SQL, specify the query used in the README ✅

`SELECT
    CONCAT(e1.Fname, ' ', e1.Lname) AS EmployeeFullName,
    e1.Super_ssn AS ManagerID,
    e2.Ssn AS EmployeeID,
    CONCAT(e2.Fname, ' ', e2.Lname) AS ManagerFullName
FROM employee AS e1
INNER JOIN employee AS e2 ON e1.Super_ssn = e2.Ssn;`

12. Merge the First Name and Last Name columns to have a single column defining employee names ✅

13. Merge department names and locations. This will make each department-location combination unique. This will assist in creating a star schema model in a future module ✅

14. Explain why, in this aforementioned case, we can only use merging and not assigning.

-> *In the scenario at hand, the most appropriate operation is "merging," as opposed to "assigning." This is because we are in the process of creating a new table or dimension that combines department and location information based on their existing values.*

*The "assigning" operation is typically applied when you want to stack tables with similar structures, while "merging" allows for creating a new table from common key columns. In this case, our goal is to create a table representing the unique relationships between departments and locations, and "merging" is the operation that excels in achieving this.*

*"Assigning" is not suitable for our purpose, as it would not result in generating unique combinations of departments and locations. Opting for "merging" allows us to create a table containing these exclusive combinations, aligning more precisely with the provided context. Therefore, "merging" is the ideal operation for creating the table we seek.*

15. Group the data to determine how many employees exist per manager ✅

16. Eliminate unnecessary columns that will not be used in the report from each table ✅


---
---

# Data Tranformation with Power BI 📋

[Português] Este relatório do Power BI é um projeto simples de visualização de dados focado na análise e apresentação de insights do banco de dados de exemplo "Company". O foco desta análise foi na limpeza e transformação de dados.

Este relatório é uma solução para o desafio [Processando e Transformando Dados com Power BII](https://web.dio.me/project/processando-e-transformando-dados-com-power-bi/learning/a23f05bd-2d61-46b8-be0e-8d2ada4ef06a?back=/track/santander-bootcamp-2023-ciencia-de-dados-com-python&tab=undefined&moduleId=undefined) proposto durante o percurso de  **Data Science** do [Santander Bootcamp](https://www.dio.me/users/nataliabrpnt)


## Tabela de Conteúdos
1. [Primeiros Passos](https://github.com/nat-brpnt/desafio_transformando_dados_power_BI/edit/main/README.md#primeiros-passos)
2. [Fonte de Dados](https://github.com/nat-brpnt/desafio_transformando_dados_power_BI/edit/main/README.md#fonte-de-dados)
3. [Deliveries Checklist](https://github.com/nat-brpnt/desafio_transformando_dados_power_BI/edit/main/README.md#deliveries-chechlist)


### Primeiros Passos
Para explorar este relatório do Power BI, siga estas etapas:

1. Pré-requisitos: Certifique-se de ter o Power BI Desktop instalado em seu computador. Se não o tiver, você pode baixá-lo [aqui](https://powerbi.microsoft.com/pt-br/downloads/).

2. Clonar ou Baixar: Clone ou baixe este repositório para o seu computador local.

3. Abrir o Relatório: Abra o arquivo "desafio_relatorio_power_BI.pbix" usando o Power BI Desktop.

4. Explorar: Interaja com o relatório, aprofunde-se nas visualizações e obtenha insights a partir dos dados financeiros.


### Fonte de Dados

O relatório é baseado nos dados fornecidos pela instrutora do curso que podem ser encontrado [em seu GitHub](https://github.com/julianazanelatto/power_bi_analyst/tree/main/M%C3%B3dulo%203/Desafio%20de%20Projeto). Este banco de dados contém informações de uma empresa fictícia, seus funcionários, departamentos, projetos, entre outros. Os dados foram pré-processados e transformados para facilitar análises e visualizações significativas.


### Deliveries Chechlist
Diretrizes para transformação dos dados

1. Verifique os cabeçalhos e tipos de dados ✅

2. Modifique os valores monetários para o tipo double preciso ✅

3. Verifique a existência dos nulos e analise a remoção ✅

4. Os employees com nulos em Super_ssn podem ser os gerentes. Verifique se há algum colaborador sem gerente ✅

5. Verifique se há algum departamento sem gerente ✅

6. Se houver departamento sem gerente, suponha que você possui os dados e preencha as lacunas ✅

7. Verifique o número de horas dos projetos ✅

8. Separar colunas complexas ✅

9. Mesclar consultas employee e departament para criar uma tabela employee com o nome dos departamentos associados aos colaboradores. A mescla terá como base a tabela employee. Fique atento, essa informação influencia no tipo de junção ✅

10. Neste processo elimine as colunas desnecessárias. ✅

11. Realize a junção dos colaboradores e respectivos nomes dos gerentes . Isso pode ser feito com consulta SQL ou pela mescla de tabelas com Power BI. Caso utilize SQL, especifique no README a query utilizada no processo. ✅

`SELECT
    CONCAT(e1.Fname, ' ', e1.Lname) AS EmployeeFullName,
    e1.Super_ssn AS ManagerID,
    e2.Ssn AS EmployeeID,
    CONCAT(e2.Fname, ' ', e2.Lname) AS ManagerFullName
FROM employee AS e1
INNER JOIN employee AS e2 ON e1.Super_ssn = e2.Ssn;`

12. Mescle as colunas de Nome e Sobrenome para ter apenas uma coluna definindo os nomes dos colaboradores ✅

13. Mescle os nomes de departamentos e localização. Isso fará que cada combinação departamento-local seja único. Isso irá auxiliar na criação do modelo estrela em um módulo futuro. ✅

14. Explique por que, neste caso supracitado, podemos apenas utilizar o mesclar e não o atribuir.

-> *No cenário em questão, a operação mais apropriada é a "mesclagem", em contraposição à "atribuição". Isso se deve ao fato de estarmos em processo de criação de uma nova tabela ou dimensão que une informações de departamentos e localizações com base em seus valores existentes.*

*A operação de "atribuir" é geralmente aplicada quando se deseja empilhar tabelas com estruturas semelhantes, enquanto a "mesclagem" permite a criação de uma nova tabela a partir de colunas-chave comuns entre as tabelas. Neste caso, nosso objetivo é criar uma tabela que represente as relações únicas entre departamentos e localizações, e é aí que a "mesclagem" se destaca.*

*A "atribuição" não é adequada para nossa finalidade, pois não resultaria na geração de combinações únicas de departamentos e localizações. Optando pela "mesclagem," conseguimos criar uma tabela que contém essas combinações exclusivas, alinhando-se de forma mais precisa com o contexto fornecido. Portanto, a "mesclagem" é a operação ideal para a criação da tabela que buscamos.*

15. Agrupe os dados a fim de saber quantos colaboradores existem por gerente ✅

16. Elimine as colunas desnecessárias, que não serão usadas no relatório, de cada tabela ✅

<br>


---

> “It's the deep breath before the plunge.”

— Gandalf

---
<div align="center">made with ❤️ by <a href="https://github.com/nat-brpnt">nat</a>.</div>
