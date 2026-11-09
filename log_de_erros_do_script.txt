======================================================================
LOG DE GERAÇÃO E INJEÇÃO DE DISTORÇÕES - COPASA (EXERCÍCIO 2025)
======================================================================
Data de Execução do Script: [Automática - via gerador_base_copasa.ipynb]
Tamanho da População Gerada: 500.000 registros
Valor Total da População (Ativo Intangível): R$ 7.179.980.000,00

MÓDULO DE INJEÇÃO DE ERROS ATIVADO
Foram injetados intencionalmente os seguintes erros na base para fins de testes de auditoria:

ID_REGISTRO | CÓDIGO | NATUREZA DO ERRO                 | VALOR DA DISTORÇÃO (R$)
---------------------------------------------------------------------------------
#045892     | ERR-01 | Superavaliação de contrato       | 80.000,00
#112405     | ERR-02 | Ausência de Suporte Documental   | 1.500.000,00
#289110     | ERR-03 | Capitalização Indevida           | 75.000,00
#356891     | ERR-04 | Falha de Corte (Cut-off)         | 320.000,00
#488102     | ERR-05 | Duplicidade de Registro          | 210.000,00
#499999     | ERR-06 | Lançamento em Feriado (Fraude)   | 5.000.000,00

======================================================================
TOTAL DE DISTORÇÕES INJETADAS (SUPERAVALIAÇÃO): R$ 7.185.000,00
STATUS: ERROS INJETADOS COM SUCESSO E SALVOS NO CSV PRINCIPAL.
======================================================================
