# Teste Analista de Dados
Critérios avaliadas:
- Uso de Funções DAX
- Documentação das medidas
- ETL
- Modelagem dimensional dos dados

### Desejáveis
- Esquema Estrela
- Criação de visuais com indicadores além dos requisitados.
- SQL (Caso deseje modelar os dados em algum banco)


### Steps:

1. Realizar um Fork desse projeto
2. Realizar a modelagem dimensional da base (Pode ser dentro do próprio PowerBI ou outra ferramenta de ETL)
    - A base está disponível para download [clicando aqui](https://download.inep.gov.br/microdados/microdados_enem_2020.zip).
    - Após descompactar a paste, o Arquivo com a base encontra-se no diretório microdados_enem_2020/DADOS/MICRODADOS_ENEM_2020.csv
    - A documentação necessária sobre os campos da base está disponível nos demais diretórios dentro da pasta descompactada.
4. Disponibilizar o link do seu repositório para posterior avaliação


### Levantar Indicadores
#### Responder às seguintes perguntas:
1. Qual a escola com a maior média de notas?
2. Qual o aluno com a maior média de notas e o valor dessa média?
3. Qual a média geral?
4. Qual o % de Ausentes?
5. Qual o número total de Inscritos?
6. Qual a média por disciplina?
7. Qual a média por Sexo?
8. Qual a média por Etnia?

-------------------------------------------------------------------------------------------------------------------------------------------------------

### Solução Atividade:
Para solucionar o desafio foi feita uma simulacao AMOSTRAL de todas as etapas e processos em ambiente real.
(Vale ressaltar que a carga TOTAL dos dados foi feita diretamente no PowerBI para análise devido tamanho da base)

#### Etapas:
1. Planejamento detalhado das ferramentas e processos
2. Analise exploratória -> Tratamento do arquivo "microdados_enem_2020.csv" pelo Alteryx (ETL)
 ![Enem2020 ETL 2](https://github.com/lucasdfbr/Teste-Analista-de-Dados-MESHA/assets/91900133/edab5e44-b5d0-4ecf-8d50-74b8bf8f7dd3)

3. Criação do banco MySQL para carga dos dados
4. Modelagem dos dados em tabelas Dimensões e fato para StarSchema:
![Modelo Starschema pbi lucas](https://github.com/lucasdfbr/Teste-Analista-de-Dados-MESHA/assets/91900133/34cfce8a-d90d-42c5-8f3d-364e19856732)

5. Consumo dos dados no PowerBI ()
6. Criação do Dashboard de análise

#### Respostas:

Link para Dashboard e Script SQL: https://drive.google.com/drive/folders/1-4P8fXCJKpWNUivQXdLZJIVJM1Ac5JBB?usp=sharing

1. Qual a escola com a maior média de notas?

R: A escola 3304557 com média 852,76.

2. Qual o aluno com a maior média de notas e o valor dessa média?

R: O aluno 200005996961 com média 858,58.

3. Qual a média geral?

R: Média geral sem redação: 512,89 ;
   Média geral com redação: 526,58

4. Qual o % de Ausentes?

R: 55,07%

5. Qual o número total de Inscritos?

R: Total de 5.783.109 inscritos

6. Qual a média por disciplina?

R: Ciências da Natureza: 490,41;
   Ciências Humanas: 511,15;
   Linguagens e Códigos: 523,80;
   Matemática: 520,58

7. Qual a média por Sexo?

R: Masculino: 535;
   Feminino: 521

8. Qual a média por Etnia?

R: Preta: 500,87;
   Parda: 508,66;
   Não Declarado: 534,05;
   Indígena: 472,84;
   Branca: 556,53;
   Amarela: 524,94
