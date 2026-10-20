# 🌵 Painel de Análise de Vendas — Sabor do Sertão

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://streamlit.io)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Painel interativo de Business Intelligence desenvolvido em **Streamlit**, **Pandas** e **Plotly** para análise das vendas de 1 ano da rede fictícia de lanchonetes regionais **Sabor do Sertão** (Recife, Olinda, Caruaru, Petrolina e Garanhuns).

---

## 📌 Sumário
- [Funcionalidades e Níveis Concluídos](#-funcionalidades-e-níveis-concluídos)
- [Estrutura do Projeto](#-estrutura-do-projeto)
- [Como Executar Localmente](#-como-executar-localmente)
- [Publicação no Streamlit Community Cloud](#-publicação-no-streamlit-community-cloud)
- [Insights Estratégicos](#-insights-estratégicos)
- [Autores / Dupla de Desenvolvimento](#-autores--dupla-de-desenvolvimento)

---

## 🚀 Funcionalidades e Níveis Concluídos

| Nível | Descrição | Status |
| :--- | :--- | :---: |
| **Passo 0** | Geração do dataset sintético com semente fixa (`gerar_dados.py`) | ✅ Concluído |
| **Nível 1** | Exploração (`head`, `describe`, `isna`) e tratamento justificado da coluna `avaliacao` (imputação por mediana) | ✅ Concluído |
| **Nível 2** | KPIs no topo com `st.metric` (Faturamento Total, Vendas, Ticket Médio, Avaliação Média) | ✅ Concluído |
| **Nível 3** | Barra lateral interativa com multiselect de cidades, categorias e seletor de intervalo de datas | ✅ Concluído |
| **Nível 4** | Visualizações em Abas com Plotly Express (Linha mensal, Barras por cidade, Top 5 produtos, Pizza de pagamentos e Mapa de calor dia x hora) | ✅ Concluído |
| **Nível 5** | 3 Conclusões analíticas para a diretoria e botão `st.download_button` para exportação do CSV filtrado | ✅ Concluído |
| **Bônus** | **Aba "Explorador Livre"**: permite carregar qualquer arquivo CSV e criar gráficos customizados escolhendo eixos X/Y e tipos de gráfico | 🌟 Concluído |

---

## 📂 Estrutura do Projeto

```text
├── app.py                      # Aplicação principal Streamlit com todos os níveis e bônus
├── gerar_dados.py              # Script gerador da base de dados de vendas (5000 linhas)
├── vendas_sabor_do_sertao.csv  # Base de dados gerada com semente 42
├── requirements.txt            # Dependências do projeto
└── README.md                   # Documentação detalhada
```

---

## 🛠️ Como Executar Localmente

### 1. Clonar o repositório
```bash
git clone https://github.com/sua-dupla/painel-sabor-do-sertao.git
cd painel-sabor-do-sertao
```

### 2. Criar e ativar o ambiente virtual (opcional, recomendado)
```bash
python -m venv venv
# Linux / macOS:
source venv/bin/activate
# Windows:
venv\Scripts\activate
```

### 3. Instalar as dependências
```bash
pip install -r requirements.txt
```

### 4. Gerar a base de dados
```bash
python gerar_dados.py
```

### 5. Executar o painel Streamlit
```bash
streamlit run app.py
```
O painel abrirá automaticamente em seu navegador padrão no endereço `http://localhost:8501`.

---

## ☁️ Publicação no Streamlit Community Cloud

Para publicar o painel gratuitamente na nuvem:
1. Faça o push de todos os arquivos para um repositório público no **GitHub**.
2. Acesse [share.streamlit.io](https://share.streamlit.io/) e faça login com sua conta do GitHub.
3. Clique em **"New app"**, selecione o repositório, branch `main` e aponte o arquivo principal para `app.py`.
4. Clique em **"Deploy"** e compartilhe o link gerado!

---

## 💡 Insights Estratégicos Identificados
1. **Recife lidera o faturamento:** Concentra ~35% das vendas da rede, acompanhado de perto por polos do interior (Caruaru e Petrolina).
2. **Predomínio do Pix:** Mais de 45% do volume financeiro das transações é transacionado via Pix, com dinheiro em espécie representando menos de 10%.
3. **Pico de Vendas:** O mapa de calor aponta forte concentração de faturamento entre 12h–14h (almoço) e 19h–21h (jantar).

---

## 👥 Autores (Pair Programming)
* **Piloto:** [Nome do Aluno 1]
* **Navegador:** [Nome do Aluno 2]

