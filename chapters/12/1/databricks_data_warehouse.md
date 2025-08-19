(databricks)=
# Capítulo 12.1 -  Configurando um Data Warehouse com Databricks

```{admonition} Atenção
Você precisará criar uma conta no [Databricks Free Edition](https://www.databricks.com/learn/free-edition) para essa parte do tutorial.

```{figure} ../../assets/img/12_1_free_edition_databricks.png

Se você tiver interesse (e conhecimento) de simular um DW *on-premises*, pode configurar um banco de dados PostgreSQL em sua máquina local.
```

Ao criarmos a conta no Databricks Free Edition uma instância de 1 thread. Então é só ligarmos a instância e estará pronta para o uso. O pŕoximo passo é criarmos nossa credencial para poder utilizar em nossas ferramentas do {ref}`MDS<MDS>` como o [Hevo](https://hevodata.com/) e [dbt](https://www.getdbt.com/).


```{figure} ../../assets/img/12_2_start_db_instance.png
:name: ativando_db

Ativando a Instância do Databricks
```

Para criar as credenciais vamos até a seção de Credenciais no “Menu API e Serviços”.

```{figure} ../../assets/img/credenciais_bq.png
:name: credenciais_db

Acessando o menu de credenciais
```

Devemos clicar no botão “Criar Credenciais” e selecionar a última opção:

```{figure} ../../assets/img/criar_credenciais_db.png
:name: criar_credenciais_db

Criar credenciais no BigQuery
```

Vamos criar uma conta de serviço para API BigQuery API. Podemos selecionar o papel “Administrador de recursos do BigQuery” para não termos problemas com permissões (em projetos reais esse papel deve ser restrito à pessoas-chave no projeto).  Colocamos um nome qualquer para a conta de serviço e o tipo JSON. Uma chave privada será criada e automaticamente baixada para seu computador. Guarde-a pois ela será utilizada futuramente para acesso ao BigQuery.

```{figure} ../../assets/img/criar_credenciais_db_2.png
:name: criar_credenciais_db_2

Criar credenciais no BigQuery
```

```{figure} ../../assets/img/criar_credenciais_db_3.png
:name: criar_credenciais_db_3

Selecione a opçao "Administrador de recursos do BigQuery"
```

```{figure} ../../assets/img/criar_credenciais_db_4.png
:name: criar_credenciais_db_4

Lembre-se de armazenar as credenciais com segurança.
```

Pronto! Você já tem uma instância do BigQuery ativada em sua conta e pode começar a armazenar e processar dados em grande escala em um *data warehouse* moderno na nuvem. Para a maioria dos casos práticos, o BigQuery é uma solução gerenciada que atende facilmente aos requisitos de projetos de *data warehouse*. Em alguns casos, especialmente com grandes volumes de dados, ele pode se tornar caro quando comparado à outras soluções de mercado. Então é bom sempre estar atento com os custos dos seus serviços na nuvem!