# PBI_atendimentos_ambulatorio
Demonstração de relatório em PowerBI para acompanhamento de atendimentos em ambulatórios
Base de dados será em excel com dados fictícios apenas para demostração de relatório interativo desenvolvido com PowerBI. (1801 linhas)

![Descrição da imagem](assets/Plan_fundo.png)

## Tratamentos Power Query

- Tipo Alterado (Definindo o tipo de cada coluna para sua devida categoria.)
- Transformando coluna TIP_ATENDIMENTO e CAT_ATENDIMENTO em maiúscula para padronização. 
- 

## Configurações de aparências
- Configurações de tela - Personalizar Altura 920px por Largura 1880px. (Tamanho com boa resolução para notebook e monitor)
- Imagem plando de fundo criado no Figma.
- Adicionado codigo para obter última atualização (let Fonte = DateTimeZone.SwitchZone(DateTimeZone.LocalNow(),-3,0) in Fonte)

## Medidas DAX

- total_atendimentos = COUNTROWS(Atendimentos)

- qtd_colaboradores = DISTINCTCOUNT(Atendimentos[MATRICULA])

- Tabela calendário basica
    ADDCOLUMNS(
    CALENDAR(DATE(2025,01,01),DATE(2025,12,01))
    ,"Ano",YEAR(
        [Date]),
        "Mês",
        MONTH([Date]),
        "Nome do Mês",
        UPPER(FORMAT([Date],
        "MMM")))