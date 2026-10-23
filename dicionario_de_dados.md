# Dicionário de Dados — Auditoria COPASA (DFP 2025)

Este documento descreve as variáveis, tipos de dados e significados das métricas e bases de amostragem utilizadas nos papéis de trabalho de auditoria (**PT 320** e **PT 530**) para a verificação de ativos da Companhia de Saneamento de Minas Gerais (COPASA).

---

## 1. Mapeamento de Parâmetros de Auditoria (`PT_320` e `PT_530`)

| Campo / Variável | Tipo de Dado | Origem / Fonte | Descrição / Regra de Negócio |
| :--- | :--- | :--- | :--- |
| `Ativo_Total_Consolidado` | Monetário (`R$`) | DFP COPASA 2025 (Balanço Patrimonial) | Valor base para a apuração da Materialidade Global do planejamento. |
| `Perc_Materialidade_Global` | Percentual (`%`) | PT 320 (Premissa de Auditoria) | Percentual aplicado sobre o Ativo Total ($1,0\%$). |
| `Materialidade_Global` | Monetário (`R$`) | Calculado (`Ativo_Total * Perc_Global`) | Limite máximo de erro tolerável para as demonstrações contábeis tomadas em conjunto ($R\$ 177.372.470,00$). |
| `Perc_Materialidade_Execucao`| Percentual (`%`) | PT 320 (Premissa de Auditoria) | Percentual de redução do risco de auditoria ($75,0\%$). |
| `Materialidade_Execucao` | Monetário (`R$`) | Calculado (`Mat_Global * Perc_Execucao`) | Alça de segurança para a execução dos procedimentos ($R\$ 133.029.352,50$). |
| `Limite_SUD` | Monetário (`R$`) | Calculado (`Mat_Global * 5%`) | Limite para acúmulo de distorções claramente insignificantes ($R\$ 8.868.623,50$). |
| `Valor_Populacao_Testada` | Monetário (`R$`) | DFP COPASA 2025 / Amostragem | Saldo da população submetida ao teste de amostragem ($R\$ 14.850.000.000,00$). |
| `Fator_Confianca` | Numérico (`Float`) | Tabela de Poisson (NBC TA 530) | Fator associado a 95% de nível de confiança ($3,0$). |
| `Intervalo_Amostragem` | Monetário (`R$`) | Calculado (`Mat_Execucao / Fator_Confianca`) | Amplitude monetária entre as seleções sistemáticas ($R\$ 44.343.117,50$). |
| `Tamanho_Amostra_Qtd` | Inteiro (`Integer`) | Calculado (`ARRED.PARA.CIMA(Populacao / Intervalo)`) | Quantidade mínima de itens/contratos selecionados para a amostra ($335\text{ itens}$). |

---

## 2. Estrutura da Base de Amostragem (`copasa_amostragem_2025.csv`)

| Coluna | Tipo de Dado | Exemplo | Descrição |
| :--- | :--- | :--- | :--- |
| `id_contrato` | Texto / String | `CT-2025-089` | Identificador único do contrato/ativo auditado. |
| `data_registro` | Data (`YYYY-MM-DD`)| `2025-05-14` | Data de contabilização do ativo no sistema patrimonial. |
| `municipio` | Texto / String | `Montes Claros` | Município mineiro vinculado à concessão/operação. |
| `categoria_ativo` | Texto / String | `Concessão Saneamento` | Classificação do item no ativo intangível/imobilizado. |
| `valor_contabil` | Monetário (`R$`) | `R$ 520.400,00` | Valor registrado no Razão Contábil do período. |
| `item_selecionado` | Booleano (`0` ou `1`)| `1` | Indicação se o registro foi capturado pelo intervalo sistemático de amostragem. |

---

## 3. Normas de Referência
* **NBC TA 320:** Materialidade no Planejamento e na Execução da Auditoria.
* **NBC TA 530:** Amostragem em Auditoria.
