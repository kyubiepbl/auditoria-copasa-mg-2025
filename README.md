# Dossiê de Auditoria - COPASA (Companhia de Saneamento de Minas Gerais)

**Universidade de Brasília — UnB**  
**Disciplina:** Auditoria 1 — CCA0024 — Turma 02 — 2026.2  
**Professor:** Lucas Oliveira Gomes Ferreira  
**Aluno(a) - Matrícula:** 222020687  
**Companhia Atribuída:** COPASA (Companhia de Saneamento de Minas Gerais - CSMG3)

---

## 📌 Objetivo do Trabalho
Este repositório contém o dossiê de auditoria da COPASA, referente ao exercício de 2025, elaborado como requisito de avaliação da disciplina de Auditoria 1. O trabalho contempla a Estrutura Conceitual e as normas NBC TA 200 a 600, integrando procedimentos reais (baseados em dados públicos da CVM/B3/RI) e procedimentos simulados para fins didáticos, utilizando uma base de dados sintética com 500.000 linhas.

---

## 📂 Organização do Repositório

O repositório está estruturado com os seguintes arquivos:

*   📄 **`dossie_auditoria_copasa.pdf`**: Dossiê completo em formato PDF contendo todos os papéis de trabalho organizados (PT EC até PT 600), com referências cruzadas, matriz de cobertura das normas, relação das fontes utilizadas e conclusão integrada.
*   📊 **`copasa_imobilizado_intangivel_2025_500k.csv`**: Base de dados simulada com 500.000 registros detalhando o Ativo Imobilizado/Intangível da COPASA (Direitos de Concessão e Infraestrutura). *(Nota: Devido ao limite de tamanho do GitHub, a base completa pode ser gerada localmente através do script abaixo ou descarregada através [deste link temporário no Google Drive / OneDrive - INSIRA SEU LINK AQUI SE NECESSÁRIO]).*
*   💻 **`gerador_base_copasa.py`**: Código-fonte em Python contendo os procedimentos necessários para a geração da base de dados sintética, além dos scripts de seleção de amostras (PT 530) e cálculos estatísticos.
*   📈 **`calculos_materialidade_amostragem.xlsx`**: Planilha editável demonstrando os cálculos de materialidade global e de execução (PT 320), conciliações e resultados da avaliação de amostras.
*   📖 **`dicionario_de_dados.md`**: Dicionário de variáveis explicando as colunas da base sintética, premissas de geração e conciliação com o saldo contábil.

---

## 🛠️ Instruções para Reprodução do Trabalho

Para reproduzir a base de dados simulada e os testes de amostragem, siga os passos abaixo:

### 1. Pré-requisitos
Certifique-se de que possui o Python instalado (versão 3.8 ou superior). As seguintes bibliotecas são necessárias:
```bash
pip install pandas numpy
