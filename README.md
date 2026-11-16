# 📊 Análise de Risco de Crédito e Perfis de Inadimplência

![Python](https://img.shields.io/badge/Python-3.13-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-3.1.1-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualização-11557c)
![Seaborn](https://img.shields.io/badge/Seaborn-Estatística-4c72b0)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)

## 📋 Sobre o Projeto
Este projeto consiste em uma **Análise Exploratória de Dados (EDA)** aplicada ao setor financeiro e de concessão de crédito. O objetivo principal é investigar os fatores comportamentais, patrimoniais e contratuais que influenciam o risco de inadimplência (*default*) e a precificação das taxas de juros.

O projeto foi desenvolvido como entrega final de análise de dados, seguindo uma metodologia estruturada desde o diagnóstico de qualidade e higienização da base até a geração de *insights* estratégicos para mitigação de perdas na carteira.

---

## 🎯 Perguntas de Negócio Respondidas
1. **Precificação de Risco:** Como as taxas de juros médias se comportam de acordo com a classificação de risco (`loan_grade`) atribuída à operação?
2. **Concentração de Capital:** Quais finalidades de empréstimo (`loan_intent`) concentram o maior volume financeiro solicitado pelos clientes?
3. **Estabilidade Patrimonial:** Qual é o impacto da situação de moradia (`person_home_ownership`) na taxa de inadimplência?
4. **Reincidência de Crédito:** Clientes com histórico prévio de inadimplência (`cb_person_default_on_file`) enfrentam juros maiores e apresentam maior propensão a novos calotes?

---

## 🗂️ Estrutura do Repositório

    ├── credit_risk_dataset/
    │   └── credit_risk_dataset.csv      # Base de dados original (Kaggle)
    ├── trabalho_final.ipynb             # Notebook principal com código, visualizações e análises
    ├── trabalho-final-enunciado.pdf     # Escopo e diretrizes do projeto
    ├── teste_ambiente.py                # Script de validação do ambiente Python
    └── README.md                        # Documentação do projeto

---

## 📖 Dicionário de Dados (Principais Variáveis)

| Variável | Descrição |
| :--- | :--- |
| `person_age` | Idade do tomador de crédito (em anos). |
| `person_income` | Renda anual declarada pelo cliente. |
| `person_home_ownership` | Situação de moradia (`RENT` - Aluguel, `OWN` - Própria, `MORTGAGE` - Hipoteca, `OTHER` - Outros). |
| `person_emp_length` | Tempo de vínculo empregatício (em anos). |
| `loan_intent` | Finalidade do empréstimo (Educação, Saúde, Empreendimento, Consolidação de Dívidas, etc.). |
| `loan_grade` | Grau de risco atribuído ao crédito (escala de **A** [menor risco] até **G** [maior risco]). |
| `loan_amnt` | Valor do empréstimo solicitado (convertido para Real - BRL utilizando câmbio de referência 1 USD = R$ 5,00). |
| `loan_int_rate` | Taxa de juros anual aplicada à operação (%). |
| `loan_status` | Status de inadimplência (`0` = Adimplente / Pago, `1` = Inadimplente / Calote). |
| `cb_person_default_on_file` | Histórico prévio de inadimplência registrado em bureaus de crédito (`Y` = Sim, `N` = Não). |

---

## 🛠️ Metodologia e Etapas Executadas

1. **Diagnóstico de Saúde da Base:** Inspeção de volumetria (32.576 registros e 12 colunas), tipagem de dados, verificação de duplicidades e mapeamento de valores ausentes.
2. **Limpeza e Tratamento Estratégico:**
   - **Tratamento de Nulos:** Identificou-se que a exclusão simples de registros nulos descartaria cerca de **9,6% a 9,8% da amostra**. Para preservar o poder estatístico e evitar viés de seleção, realizou-se a imputação utilizando **medianas agrupadas** por perfil.
   - **Remoção de Outliers:** Filtragem de inconsistências cadastrais (como idades irreais acima de 100 anos).
   - **Engenharia de Atributos e Localização:** Conversão monetária para Reais (BRL) e tradução de categorias e legendas para o português.
3. **Análise Exploratória e Visualização:** Cruzamento estatístico com tabelas resumo e gráficos comparativos desenvolvidos com `Matplotlib` e `Seaborn`.

---

## 💡 Principais Conclusões e Insights de Negócio

* **Precificação Eficiente de Risco:** A instituição eleva progressivamente a taxa de juros conforme o grau de risco migra de **A** para **G**, compensando a maior exposição ao risco por meio de taxas mais altas.
* **O Peso do Histórico Prévio:** Clientes com registro anterior de restrições (`cb_person_default_on_file = Y`) apresentam uma taxa de inadimplência atual de **37,81%** (mais que o dobro dos **18,40%** observados em clientes sem histórico negativo), além de arcarem com juros médios superiores (**14,51%** contra **10,26%**).
* **Lastro Patrimonial como Mitigador:** Tomadores com imóvel próprio (`OWN`) ou financiado (`MORTGAGE`) demonstram menor propensão ao calote em comparação aos que residem de aluguel (`RENT`). A categoria atípica `OTHER` apresentou taxa elevada devido à menor estabilidade patrimonial e ao efeito estatístico de amostra reduzida.
* **Recomendações:** Implementação de travas de aprovação e exigência de garantias reais para operações nos graus **E, F e G** ou com histórico prévio negativo, direcionando campanhas de retenção para os perfis de baixo risco.

---

## 🚀 Como Executar o Projeto Localmente

1. Clone este repositório:
   git clone [https://github.com/RonaldoJW/Projeto.git](https://github.com/RonaldoJW/Projeto.git)
2. Acesse a pasta do projeto:
   cd Projeto
3. Certifique-se de ter as bibliotecas instaladas:
   pip install pandas numpy matplotlib seaborn jupyter
4. Abra o arquivo trabalho_final.ipynb no VS Code ou Jupyter Notebook e execute todas as células (Run All).

---

## 👤 Autor
**Ronaldo Garibaldi Monteiro**  
*Analista de Dados | Projeto #1772 CAIXAVERSO - FC6*
