
---

# 📊 Auditoria de Dados COPASA - Ativo Intangível (2025)

**Autor:** Denzel Pereira Santos — Matrícula: 222020687
**Disciplina:** Auditoria 1 — CCA0024 — Turma 02
**Professor:** Lucas Oliveira Gomes Ferreira
**Universidade de Brasília (UnB) - Departamento de Ciências Contábeis e Atuariais**

---

## 🎯 Objetivo do Projeto

Este repositório contém os artefatos de um trabalho prático de **auditoria independente** e **análise de dados** focado no **Ativo Intangível** da Companhia de Saneamento de Minas Gerais (COPASA), simulando o exercício findo em **31/12/2025**.

O projeto integra conceitos de contabilidade societária, normas de auditoria (NBC TA) e programação (Python, Pandas) para realizar **testes substantivos automatizados** em um grande volume de dados (Data Analytics), demonstrando na prática a aplicação da **NBC TA 530 (Amostragem em Auditoria)** e da **NBC TA 450 (Avaliação de Distorções)**.

**Contexto Real da Companhia:** Os dados financeiros base (materialidade, receitas, provisões) foram extraídos das Demonstrações Financeiras Padronizadas (DFP) reais de 2025 da COPASA, auditadas pela Grant Thornton. O planejamento considerou os Principais Assuntos de Auditoria (KAMs) apontados pelos auditores reais (Capitalização de Custos, Receita Não Medida e Provisões) e os riscos regulatórios do processo de Desestatização (Lei Estadual nº 25.664/2025).

---

## 📂 Estrutura do Repositório

| Arquivo | Descrição |
| :--- | :--- |
| **`dossie_auditoria_copasa.pdf`** | Relatório final de asseguração (Dossiê) detalhando os 27 Papéis de Trabalho (PTs), desde a estrutura conceitual (PT-EC) até a auditoria de grupos (PT-600). |
| **`gerador_base_copasa.ipynb`** | Notebook Jupyter em Python responsável por gerar a população sintética (500k linhas), inserir distorções controladas (ERR-01 a ERR-06) e simular os testes de auditoria (CAATs). |
| **`copasa_imobilizado_intangivel_2025_500k.csv`** | Base de dados sintética principal, com 500.000 registros de adições ao Ativo Intangível (calibrada em R$ 7.179.980.000,00). |
| **`log_erros_inseridos.txt`** | Gabarito contendo o registro exato das distorções provocadas pelo script para validação dos testes (Taxa de Detecção de 100%). |
| **`dicionario_de_dados.md`** | Documento com o mapeamento das variáveis da base sintética (ID, Data, Município, Conta Débito/Crédito, etc.). |
| **`COPASA_PT320_PT530_Materialidade_Amostragem.xlsx`** | Planilha editável com os cálculos de materialidade (MG, ME, SUD) e o dimensionamento da amostragem MUS (162 itens). |

---

## 🔢 Parâmetros da Auditoria (Resumo)

A tabela abaixo resume as métricas-chave do planejamento de auditoria, conforme detalhado no dossiê (PT-320 e PT-530).

| Parâmetro | Critério Aplicado | Valor Calculado (R$) |
| :--- | :--- | :--- |
| **Base de Cálculo** | Total do Ativo Consolidado (2025) | 17.737.247.000,00 |
| **Materialidade Global** | 1% da Base de Cálculo | **177.372.470,00** |
| **Materialidade de Execução** | 75% da Materialidade Global | **133.029.352,50** |
| **Limite de Distorções (SUD)** | 5% da Materialidade Global | **8.868.623,50** |
| **População Testada** | Ativo Intangível (500.000 linhas) | 7.179.980.000,00 |
| **Amostra Estatística (MUS)** | NBC TA 530 (95% confiança, 0 erros esperados) | **162 itens** |

> **Nota:** O total de distorções factuais identificadas na amostra foi de **R$ 7.185.000,00**, valor quantitativamente abaixo do SUD, porém exigindo análise qualitativa e comunicação à governança devido ao indício de fraude no lançamento ERR-06 (R$ 5.0 milhões em feriado).

---

## ⚙️ Como Executar o Projeto

Para reproduzir a base de dados e os testes de auditoria, siga os passos abaixo:

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/seu-usuario/auditoria-copasa-2025.git
   ```

2. **Instale as dependências:**
   Certifique-se de ter o **Python 3.9+** e as bibliotecas `pandas`, `numpy` e `jupyter` instaladas.
   ```bash
   pip install pandas numpy jupyter openpyxl
   ```

3. **Execute o Notebook:**
   Abra o arquivo `gerador_base_copasa.ipynb` no Jupyter Notebook ou Google Colab e execute todas as células.
   ```bash
   jupyter notebook gerador_base_copasa.ipynb
   ```

4. **Verifique os resultados:**
   Os arquivos `.csv` e `.txt` serão gerados automaticamente no diretório raiz. A semente (seed) utilizada é `222020687` para garantir a reprodutibilidade exata dos dados.

---

## 📚 Referências Normativas e Fontes

* **Fontes de Auditoria:** DFP COPASA 2025 (CVM), Relatório do Auditor Independente (Grant Thornton) e Resoluções ARSAE-MG.
* **Normas Aplicadas:** NBC TA Estrutura Conceitual, NBC TA 200 a 600 (CFC).

---

## ✒️ Autor

**Denzel Pereira Santos**
Matrícula: 222020687
Universidade de Brasília (UnB)

---

## 📝 Licença

Este projeto é de uso estritamente acadêmico, desenvolvido para a disciplina de Auditoria 1 da UnB. A base de dados gerada é 100% sintética e não representa movimentações reais da COPASA.
