# Dossiê de Auditoria - COPASA (Companhia de Saneamento de Minas Gerais)

**Universidade de Brasília — UnB**  
**Disciplina:** Auditoria 1 — CCA0024 — Turma 02 — 2026.2  
**Professor:** Lucas Oliveira Gomes Ferreira  
**Aluno - Matrícula:** Denzel Pereira Santos (222020687)  
**Companhia Atribuída:** COPASA (CSMG3) - Exercício 2025

---

## 📌 Objetivo do Trabalho
Este repositório contém o dossiê de auditoria da COPASA, referente ao exercício de 2025. O trabalho contempla a Estrutura Conceitual e as normas NBC TA 200 a 600, integrando procedimentos reais (baseados em dados públicos da CVM e RI) e procedimentos simulados, utilizando uma base de dados sintética de 500.000 linhas validada por testes estatísticos de amostragem.

## 📂 Estrutura do Repositório

Os arquivos entregues estão organizados da seguinte forma:

*   📊 **`COPASA_PT320_PT530_Materialidade_Amostragem.xlsx`**: Planilha com os cálculos de materialidade e o dimensionamento do teste de amostragem (população corrigida de R$ 14,85 bilhões e amostra de 335 itens).
*   📖 **`README.md`**: Este arquivo de documentação e guia do projeto.
*   🗄️ **`copasa_imobilizado_intangivel_2025_500k`**: Base de dados sintética obrigatória com 500.000 registros analíticos referentes aos ativos de infraestrutura e concessão.
*   📋 **`dicionario_de_dados.md`**: Dicionário detalhado das variáveis da base, métricas de amostragem e catálogo de erros.
*   📄 **`dossie_auditoria_copasa.pdf`**: Dossiê de auditoria completo (Volume Final) contendo todos os papéis de trabalho (PT EC a PT 600), devidamente estruturados e cruzados.
*   💻 **`gerador_base_copasa.ipynb`**: Notebook em Python (Google Colab) utilizado para a criação da base de 500.000 linhas e injeção controlada de distorções.
*   📝 **`log_erros_inseridos.txt`**: Registro exato em formato texto (CSV) das exceções, ausências de suporte e falhas de cut-off inseridas propositalmente na base para a aplicação da NBC TA 530.

## 🛠️ Instruções para Reprodução
O projeto pode ser integralmente reproduzido executando o arquivo `gerador_base_copasa.ipynb` em ambiente Colab ou Jupyter. Todos os saldos testados e falhas mapeadas no `log_erros_inseridos.txt` foram parametrizados para demonstrar a adequação dos controles e limites de distorção apurados no `dossie_auditoria_copasa.pdf`.
