# PBI_atendimentos_ambulatorio
Demonstração de relatório em PowerBI para acompanhamento de atendimentos em ambulatórios

Base de dados será em excel com dados fictícios apenas para demostração de relatório interativo desenvolvido com PowerBI. (1801 linhas)

## Tratamentos Power Query

- Tipo Alterado (Definindo o tipo de cada coluna para sua devida categoria.)
- Transformando coluna TIP_ATENDIMENTO e CAT_ATENDIMENTO em maiúscula para padronização. 

## Configurações de aparências
- Configurações de tela - Personalizar Altura 920px por Largura 1880px. (Tamanho com boa resolução para notebook e monitor)


## Medidas DAX

- total_atendimentos = COUNTROWS(Atendimentos)
- qtd_colaboradores = DISTINCTCOUNT(Atendimentos[MATRICULA])