
---

# 📊 Auditoria de Dados COPASA - Ativo Intangível (2025)

**Autor:** Denzel Pereira Santos
**Disciplina:** Auditoria 1
**Professor:** Lucas Oliveira Gomes Ferreira
**Universidade de Brasília (UnB) - Departamento de Ciências Contábeis e Atuariais**

---

## 🎯 Objetivo do Projeto

Este repositório contém os artefatos de um trabalho prático de **auditoria independente** e **análise de dados** focado no **Ativo Intangível** da Companhia de Saneamento de Minas Gerais (COPASA), simulando o exercício findo em **31/12/2025**.

O projeto integra conceitos de contabilidade societária, normas de auditoria (NBC TA) e programação (Python, Pandas) para realizar **testes substantivos automatizados** em um grande volume de dados (Data Analytics), demonstrando na prática a aplicação da **NBC TA 530 (Amostragem em Auditoria)** e da **NBC TA 450 (Avaliação de Distorções)**.

---

## 📂 Estrutura do Repositório

| Arquivo | Descrição |
| :--- | :--- |
| **`dossie_auditoria_copasa.pdf`** | Relatório final de asseguração detalhando os Papéis de Trabalho (PTs), desde a materialidade (PT 320) até a avaliação de distorções (PT 450). |
| **`gerador_base_copasa.ipynb`** | Notebook Jupyter em Python responsável por gerar a população sintética, inserir distorções controladas e simular os testes de auditoria. |
| **`copasa_imobilizado_intangivel_2025_500k.csv`** | Base de dados principal (gerada pelo script), com 500.000 registros de adições ao Ativo Intangível. |
| **`log_erros_inseridos.txt`** | Gabarito contendo o registro exato das distorções provocadas pelo script para validação dos testes. |

---

## 🔢 Parâmetros da Auditoria (Resumo)

A tabela abaixo resume as métricas-chave do planejamento de auditoria, conforme detalhado no dossiê (PT 320 e PT 530).

| Parâmetro | Critério Aplicado | Valor Calculado (R$) |
| :--- | :--- | :--- |
| **Base de Cálculo** | Total do Ativo Consolidado (2025) | 17.737.247.000,00 |
| **Materialidade Global** | 1% da Base de Cálculo | **177.372.470,00** |
| **Materialidade de Execução** | 75% da Materialidade Global | **133.029.352,50** |
| **Limite de Distorções (SUD)** | 5% da Materialidade Global | **8.868.623,50** |
| **População Testada** | Ativo Intangível (Adições) | 7.179.980.000,00 (500.000 linhas) |
| **Amostra Estatística (MUS)** | NBC TA 530 (95% confiança, 0 erros esperados) | **162 itens** |

> **Nota:** O total de distorções factuais encontradas foi de **R$ 7.185.000,00**, valor quantitativamente abaixo do SUD, porém exigindo análise qualitativa devido ao indício de fraude (NBC TA 450, item A21).

---

## ⚙️ Como Executar o Projeto

Para reproduzir a base de dados e os testes de auditoria, siga os passos abaixo:

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/seu-usuario/auditoria-copasa-2025.git
    ```

2.  **Instale as dependências:**
    Certifique-se de ter o **Python 3.9+** e as bibliotecas `pandas`, `numpy` e `jupyter` instaladas.
    ```bash
    pip install pandas numpy jupyter
    ```

3.  **Execute o Notebook:**
    Abra o arquivo `gerador_base_copasa.ipynb` no Jupyter Notebook ou Google Colab e execute todas as células.
    ```bash
    jupyter notebook gerador_base_copasa.ipynb
    ```

4.  **Verifique os resultados:**
    Os arquivos `copasa_imobilizado_intangivel_2025_500k.csv` e `log_erros_inseridos.txt` serão gerados automaticamente no diretório raiz do projeto.

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.9+**
- **Pandas** (Manipulação e análise de dados)
- **Numpy** (Geração de dados estatísticos)
- **Jupyter Notebook** (Ambiente de desenvolvimento interativo)

---

## 📚 Referências Normativas

- **NBC TA 320 (R1):** Materialidade no Planejamento e na Execução da Auditoria.
- **NBC TA 450 (R1):** Avaliação das Distorções Identificadas durante a Auditoria.
- **NBC TA 530:** Amostragem em Auditoria.
- **NBC TA 240 (R1):** Responsabilidade do Auditor em Relação a Fraude.

---

## ✒️ Autor

**Denzel Pereira Santos**
Matrícula: 222020687
Universidade de Brasília (UnB)

---

## 📝 Licença

Este projeto é de uso estritamente acadêmico, desenvolvido para a disciplina de Auditoria 1 da UnB.
