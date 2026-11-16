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

```text
├── credit_risk_dataset/
│   └── credit_risk_dataset.csv      # Base de dados original (Kaggle)
├── trabalho_final.ipynb             # Notebook principal com código, visualizações e análises
├── trabalho-final-enunciado.pdf     # Escopo e diretrizes do projeto
├── teste_ambiente.py                # Script de validação do ambiente Python
└── README.md                        # Documentação do projeto
