<h1>Projeto em Dados - Obesidade</h1>

<h1>Introdução</h1>

Este projeto tem como objetivo analisar fatores que influenciam a obesidade utilizando o conjunto de dados público, retirado do Kaggle.

<hr>
<br>

<h1>Entendendo a base de dados</h1>
O conjunto de dados contém informações relacionadas a fatores que podem influenciar a obesidade, incluindo:

<b>Características pessoais:</b> 
- Gênero

- Idade

- Altura

- Peso.

<b>Hábitos alimentares:</b> 
- Frequência de consumo de fast food (FAVC)

- Consumo de vegetais (FCVC)

- Número de refeições diárias (NCP)

- Consumo de álcool (CALC).

<b>Estilo de vida:</b> 
- Nível de atividade física (FAF)

- Tempo de uso de tecnologia (TUE)

- Se fuma ou não (SMOKE)

- Histórico familiar de obesidade (family_history).

Modo de transporte (MTRANS)

Obesity, categorizando as pessoas em diferentes níveis de obesidade.

<hr>
<br>

<h1>Tecnologias Utilizadas</h1>

<b>Linguagem:</b> Python

<h3><b>Bibliotecas:</b></h3>

<b>Pandas:</b> Manipulação e análise de dados

<b>Seaborn e Matplotlib:</b> Visualização de dados

<b>Streamlit:</b> Criação do dashboard interativo

<b>Sklearn:</b> Implementação do modelo de Machine Learning (Random Forest Classifier)

<br>

<h2><b>Estrutura do Dashboard</b></h2>
O dashboard é dividido em quatro páginas. 

<br>

<h2><b>Visão Geral</b></h2>
Nesta seção, são apresentados gráficos sobre a distribuição do Índice de Massa Corporal (IMC) e a frequência das diferentes categorias de obesidade.

<h3><b>Distribuição do IMC</b></h3> 
Mostra a distribuição do IMC na base de dados.

```python
fig, ax = plt.subplots()
    sns.histplot(df['BMI'], bins=30, kde=True, ax=ax)
    st.pyplot(fig)
```
![Graf 1 pag 1](https://github.com/user-attachments/assets/5d768434-7260-47de-865a-383980ea1dd5)

<br>

<h3><b>Contagem das Categorias de Obesidade</b></h3> 
Representa a quantidade de indivíduos em cada categoria de obesidade.

```python
fig, ax = plt.subplots()
    sns.countplot(data=df, x='Obesity', ax=ax)
    plt.xticks(rotation=45)
    st.pyplot(fig)
```
![Graf 2 pag 1](https://github.com/user-attachments/assets/c5aadff3-35ac-41b2-9f97-e60cf7ba6c7c)

<br>

<h2><b>Hábitos Alimentares</b></h2>
Explora a relação entre obesidade e os hábitos alimentares dos indivíduos.

<h3><b>FCVC vs Obesidade</b></h3> 
Avalia o consumo de vegetais por nível de obesidade.

```python
  fig, ax = plt.subplots()
    sns.boxplot(data=df, x='Obesity', y='FCVC', ax=ax)
    plt.xticks(rotation=45)
    st.pyplot(fig)
```
![Graf 1 pag 2](https://github.com/user-attachments/assets/cd3cf9d4-2b75-45a1-8472-aca6c867dd2a)

<br>

<h3><b>Contagem FAVC vs Obesidade</b></h3> 
Analisa a relação entre o consumo frequente de fast food e a obesidade.

```python
fig, ax = plt.subplots()
    sns.countplot(data=df, x='FAVC', hue='Obesity', ax=ax)
    st.pyplot(fig)
```
![Graf 2 pag 2](https://github.com/user-attachments/assets/9f5c9004-5f5e-45f7-baf0-88da57a2951f)

<br>

<h2><b>Estilo de Vida</b></h2>
Foca no impacto do estilo de vida na obesidade.

<h3><b>FAF vs Obesidade</b></h3> 
Examina a relação entre nível de atividade física e obesidade.

```python
fig, ax = plt.subplots()
    sns.boxplot(data=df, x='Obesity', y='FAF', ax=ax)
    plt.xticks(rotation=45)
    st.pyplot(fig)
```
![Graf 1 pag 3](https://github.com/user-attachments/assets/f5a164e5-b4ec-4c7d-b2a9-68c12a8a4c80)

<br>

<h3><b>TUE vs Obesidade</b></h3> 
Analisa o impacto do tempo de uso de dispositivos eletrônicos.

```python
   fig, ax = plt.subplots()
    sns.boxplot(data=df, x='Obesity', y='TUE', ax=ax)
    plt.xticks(rotation=45)
    st.pyplot(fig)

```
![Graf 2 pag 3](https://github.com/user-attachments/assets/0bd3ed4c-4c97-44c2-8b7e-16fb267d6ea9)

<hr>
<br>

<h1>Possíveis Melhorias Futuras</h1>

Adição de modelos de Machine Learning para comparação de desempenho.

Análise mais aprofundada de correlações entre variáveis.

Integração com banco de dados para armazenamento dinâmico dos dados.

<hr>
