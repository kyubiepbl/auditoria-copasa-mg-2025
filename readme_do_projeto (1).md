# Auditoria de Dados COPASA - Ativo Intangível (2025)

**Autor:** Denzel Pereira Santos
**Disciplina:** Finanças Corporativas 2 / Dados Abertos UnB (Adaptação para Auditoria Contábil)
**Professor:** Lucas Oliveira Gomes Ferreira

## Descrição do Projeto
Este repositório contém os artefatos de um trabalho prático de auditoria independente e análise de dados focado no **Ativo Intangível** da Companhia de Saneamento de Minas Gerais (COPASA), simulando o exercício findo em 31/12/2025. 

O projeto une conceitos de contabilidade societária, normas de auditoria (NBC TA) e o uso de programação (Python, Pandas) para testes substantivos automatizados de grande volume de dados (Data Analytics).

## Arquivos do Repositório

1. **`dossie_auditoria_copasa.pdf`**: O relatório final de asseguração detalhando os Papéis de Trabalho (PTs), desde a materialidade (PT 320) até a avaliação de distorções (PT 450).
2. **`gerador_base_copasa.ipynb`**: Notebook Jupyter em Python responsável por:
   - Gerar uma população sintética de 500.000 registros representando as adições ao Ativo Intangível da COPASA.
   - Inserir distorções intencionais controladas (erros de cut-off, duplicidade, e fraude em feriado) para serem "descobertas" nas rotinas de auditoria.
3. **`copasa_imobilizado_intangivel_2025_500k.csv`** *(Gerado pelo script)*: A base de dados principal.
4. **`log_erros_inseridos.txt`**: O gabarito contendo o registro exato dos erros provocados pelo script para fins de validação dos testes.

## Parâmetros da Auditoria (Resumo)

* **População Base (Ativo Intangível):** R$ 7.179.980.000,00 (500.000 linhas)
* **Materialidade Global (1% do Ativo):** R$ 177.372.470,00
* **Materialidade de Execução (75% da Global):** R$ 133.029.352,50
* **Limite para Desconsideração (SUD):** R$ 8.868.623,50
* **Amostra Estatística (MUS - NBC TA 530):** 162 itens selecionados
* **Total de Distorções Factuais Encontradas:** R$ 7.185.000,00 (Quantitativamente abaixo do SUD, porém exigindo análise qualitativa por indício de fraude).

## Como Executar
1. Clone o repositório.
2. Certifique-se de ter o Python 3.9+ e as bibliotecas `pandas` e `numpy` instaladas.
3. Execute todas as células do arquivo `gerador_base_copasa.ipynb`.
4. Os arquivos `.csv` e `.txt` serão gerados automaticamente no mesmo diretório.