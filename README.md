# 📉 Análise de Churn - TelecomX BR

Um projeto completo de Ciência de Dados com foco na extração, transformação e análise de dados para entender a taxa de evasão (Churn) de clientes em uma empresa de telecomunicações fictícia, a TelecomX.

## 📖 Sobre o Projeto

A evasão de clientes é um dos maiores desafios para empresas que operam sob um modelo de assinaturas. O objetivo deste projeto é analisar a base de dados da TelecomX para identificar a proporção de clientes que cancelaram seus serviços, limpar e adequar os dados para futuras modelagens preditivas e gerar visualizações iniciais que ajudem na tomada de decisão.

## 🛠️ Tecnologias Utilizadas

Neste projeto, utilizei Python e as principais bibliotecas do ecossistema de Data Science:
- **[Pandas](https://pandas.pydata.org/):** Limpeza, manipulação e transformação dos dados.
- **[Requests](https://requests.readthedocs.io/):** Consumo de dados diretamente de uma API/URL em formato JSON.
- **[Matplotlib](https://matplotlib.org/) & [Seaborn](https://seaborn.pydata.org/):** Criação de gráficos e visualizações de dados.

## ⚙️ Etapas do Projeto

O projeto foi estruturado em três etapas principais:

### 1. 📌 Extração
- Leitura dos dados brutos hospedados em um repositório remoto via requisição HTTP (formato JSON).
- Conversão da estrutura JSON aninhada em um formato tabular usando o `pd.json_normalize()`.

### 2. 🔧 Transformação e Limpeza
- **Tratamento de Dados Ausentes:** Identificação e tratamento de valores nulos (ex: conversão da coluna `account.Charges.Total` para o formato numérico e preenchimento de inconsistências).
- **Remoção de Colunas Desnecessárias:** O campo `customerID` foi removido por não possuir peso analítico após a validação de que não haviam clientes duplicados.
- **Padronização:** Renomeação das colunas do inglês para o português, substituindo pontos por *underscores* para facilitar a manipulação no Python.
- **Engenharia de Atributos (Feature Engineering):** Criação de novas métricas, como o `Valor por dia` (Contas Diárias) e a categorização em faixas do `Tempo de contrato` (0-1 Ano, 1-2 Anos, etc.).
- **Encoding Básico:** Mapeamento de variáveis categóricas binárias ('Yes' e 'No') para representações numéricas (1 e 0).

### 3. 📊 Análise e Visualização
- Exploração estatística rápida (Média, Desvio Padrão, Máximos e Mínimos) utilizando o `describe()`.
- Cálculo exato da Taxa de Evasão (Churn) da empresa.
- Criação de um gráfico de pizza customizado utilizando Seaborn e Matplotlib para visualizar a proporção de clientes retidos versus clientes que saíram.

## 💡 Principais Resultados

- **Taxa de Evasão Geral:** Foi identificado que a TelecomX possui uma taxa de evasão de **25.72%**.
- A base de dados resultante (7.267 linhas e 22 colunas limpas) está totalmente traduzida, sem valores nulos e tipada corretamente, servindo perfeitamente como insumo para a criação de um modelo de *Machine Learning* no futuro.

## 🚀 Como Executar

1. Clone o repositório:
```
   git clone [https://github.com/seu-usuario/nome-do-repositorio.git](https://github.com/seu-usuario/nome-do-repositorio.git)

```

2. Instale as dependências necessárias:
```
    pip install pandas matplotlib seaborn requests

```


3. Abra o arquivo Jupyter Notebook (`TelecomX_BR Final`) e execute as células sequencialmente.

---

Desenvolvido por **André Vinicius**. Sinta-se à vontade para conectar-se comigo ou enviar sugestões!


Autor: André Vinicius Silva Santos LinkedIn: www.linkedin.com/in/andreviniss
