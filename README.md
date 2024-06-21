## [DIO][Desafio] Star Schema - Professor

**DIO - Bootcamp Data Analytics com Power BI - Star Schema - Professor**

## Descrição do Projeto:

Criar o diagrama dimensional – star schema – com base no diagrama relacional disponibilizado. Com foco na análise dos dados dos professores.

Deverá ser criada a tabela Fato que contém o contexto analisado. Da mesma forma, é necessária a criação das tabelas dimensão que serão compostas pelos detalhes  relacionados ao contexto.

Criar uma tabela dimensão de datas para compensar a falta de dados de datas do modelo relacional, supondo que você tem acesso aos dados e criar os campos necessários para modelagem.

**Imagem de referência fornecida:**

![image](https://github.com/christianalencar/DIO-Desafio-Star_Schema_Professor/assets/100319396/daa5c09e-cb24-4964-b2fd-2c2da641b4fc)


## Partes do modelo do Star Schema - Professor

1. **Tabela Fato (fprofessor)**:

    - **id_professor**: Chave estrangeira referenciando a dimensão do Professor.
    - **id_curso**: Chave estrangeira referenciando a dimensão do Curso.
    - **id_departamento**: Chave estrangeira referenciando a dimensão do Departamento.
    - **id_data**: Chave estrangeira referenciando a dimensão de Data.
    - **aulas_qtd**: Quantidade de aulas ministradas.
    - **aulas_hora**: Total de horas de ensino.
    - **avaliacao_media**: Valor da média da avaliação recebida
    - **salario**: Valor salarial do professor.

2. **Lista de Tabelas de Dimensão**:

    2.1 - **dim_professor**:
   
      - **id_professor**: Chave primária.
      - **nome_primeiro**: Primeiro nome do professor.
      - **nome_sobrenome**: Sobrenome do professor.
      - **genero**: Gênero declarado pelo professor.
      - **grau_Acadêmico**: Grau acadêmico mais alto do professor.
      - **data_contratação**: Data de contratação do professor.

    2.2 - **dim_curso**:
   
      - **id_curso**: Chave primária.
      - **nome_curso**: Nome do curso.
      - **qtd_creditos**: Quantidade de créditos do curso.
      - **duracao_semanas**: Duração do curso em semanas.

    2.3 - **dim_departamento**:
   
      - **id_departamento**: Chave primaria.
      - **nome_departamento**: Nome do departamento.
      - **nome_faculdade**: Nome da faculdade que o departamento é ligado.
  
     2.4 - **dim_data**

      - **id_data**: Chave primária.
      - **data**: Data em formato padrão
      - **ano**: Ano da data.
      - **mes**: Mês da data.
      - **dia**: Dia do mês da data.
      - **trimestre**: Trimestre da data.
  
**Star Schema no  MySQl Workbench**

![star_chema_professor](https://github.com/christianalencar/DIO-Desafio-Star_Schema_Professor/assets/100319396/009a5610-c131-47bb-9ce9-d98fd2f23505)

## Procedimento

Criação da tabela dimensional data para complementar as informações para relacionamentos e consultas;

Modelagem, criação a partir das informações do schema original para criação de acordo com o perfil necessário;

Documentação, em ambiente de teste fazer a documentação necessária para registro e acompanhamento posterior


   
