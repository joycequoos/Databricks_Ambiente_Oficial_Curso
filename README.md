# Databricks Ambiente Oficial Curso

1) Criar o Catalog: curso_databricks,
2) Criar o Schema: curso_databricks.aula
3) Criar o Volume: curso_databricks.aula.aula_volume
 
  <img width="784" height="414" alt="image" src="https://github.com/user-attachments/assets/1c88e010-1391-4a4d-ac3e-fc4ec7bffafa" />

  <img width="360" height="489" alt="image" src="https://github.com/user-attachments/assets/4daa00d3-85f2-419f-91cf-259dc0ce38e5" />

  https://github.com/joycequoos/Databricks_Ambiente_Oficial_Curso/blob/main/01.Criando%20Schema%20e%20Volume.py

  # Importando Arquivos para Volumes

1) Selecionar o arquivo e arrastar em volume já funciona

<img width="977" height="462" alt="image" src="https://github.com/user-attachments/assets/2b18699c-a20e-4148-b581-6733cb46c8af" />

2) Volumes criados

<img width="825" height="564" alt="image" src="https://github.com/user-attachments/assets/5db0e576-9cb1-4725-89a9-941db5131786" />

Vamos pegar os dados, transformar e salvar em tabelas, em arquivos de outros formatos, com isso entenderemos essa manipulacao de arquivos dentro do Databricks

https://github.com/joycequoos/Databricks_Ambiente_Oficial_Curso/blob/main/01.Primeiros%20comandos.py

<img width="727" height="575" alt="image" src="https://github.com/user-attachments/assets/47eb55d7-5475-4680-90c1-14933fc7bc0f" />

- Executando comandos dbutils

<img width="712" height="246" alt="image" src="https://github.com/user-attachments/assets/2d7402c8-5f8b-49e2-859f-25878c1091c7" />

- Utilizando comando display para deixar mais amigavel a visualizacao dos dados

<img width="707" height="402" alt="image" src="https://github.com/user-attachments/assets/ea68994b-bae3-4408-a423-5040ef176b0f" />

- Verificando dentro da pasta Bike Sore

<img width="1196" height="552" alt="image" src="https://github.com/user-attachments/assets/f6dc0dc2-8800-48da-9334-169957277461" />

- Lendo um arquivo, diretamente do diretorio

<img width="1200" height="461" alt="image" src="https://github.com/user-attachments/assets/c68124d2-8d82-40b7-8f0d-677291ce0e69" />

- Utilizando o modo Display

<img width="1218" height="499" alt="image" src="https://github.com/user-attachments/assets/dc03fd87-ba8d-4ba1-bacc-477990d7f687" />

### Manipulando Dataframe Databricks

Um DataFrame no Databricks é uma estrutura de dados bidimensional distribuída, organizada em colunas com nomes e tipos definidos, similar a uma tabela de banco de dados relacional ou a uma planilha do Excel.

No ecossistema do Databricks, que é construído sobre o Apache Spark, os DataFrames são a principal abstração para manipulação e processamento de dados em grande escala (Big Data).

Exemplo de Uso (PySpark vs. SQL)
No Databricks, você pode criar e consultar DataFrames facilmente usando Python ou SQL diretamente nos Notebooks:

Criando e filtrando em Python (PySpark):

<img width="723" height="260" alt="image" src="https://github.com/user-attachments/assets/d4ab4391-7274-42e9-9ea0-7b7caa9ec086" />

- Consultando o mesmo dataframe em SQL

<img width="749" height="274" alt="image" src="https://github.com/user-attachments/assets/a9d56984-7d54-4914-bc35-5e4fa886e64e" />

Aqui vamos estar utilizando a arquitetura do Spark, lendo dados com spark

<img width="1200" height="419" alt="image" src="https://github.com/user-attachments/assets/4a680dc6-0376-450f-8b8d-7e1e5e52cf21" />

### Dados Públicos Para Treino databricks+datasets+kaggle

<img width="711" height="223" alt="image" src="https://github.com/user-attachments/assets/0b6b54b3-322a-4eab-a60d-9b79a6f63332" />

https://www.kaggle.com

- Datasets que o próprio Databricks deixa disponivel para trabalhar:

  <img width="1192" height="614" alt="image" src="https://github.com/user-attachments/assets/b9e2740d-41a9-49f9-b596-a64f158d3b09" />

- Lendo um dataset

<img width="1204" height="377" alt="image" src="https://github.com/user-attachments/assets/48b452ed-6e7f-468d-8155-9b69020cb31a" />

- Lendo um arquivo de um Dataset do Databricks

<img width="1206" height="672" alt="image" src="https://github.com/user-attachments/assets/32198b7f-1b1c-4a6c-80a5-4abf2b1f25d8" />

- Lendo e escrevendo arquivos em um diretório

<img width="1546" height="350" alt="image" src="https://github.com/user-attachments/assets/aa2d38a0-f0e5-48d0-9a1f-e13630b26085" />

### Criando Tabelas

  


