# BootcampAlura_ProjetoModulo1
## Análise dos dados de procedimentos hospitalares do SUS
Olá! Bem vindo ao meu repositório do projeto módulo 1 do bootcamp de data science Alura!
### Como navegar
1. Sugiro primeiramente ler o README inteiro, aqui já terá um resumo de tudo!
2. A pasta Bases estão todas as bases utilizadas na análise, elas foram obtidas no DataSUS - TabNet, bem como no IBGE
3. A pasta Notebooks estão os Notebooks criados para as análises, se for abrir sugiro fazer na sequência numérica
### Sobre os dados
. Os dados do DataSUS foram todos levantados pela trazendo a data do atendimento, puxando os processamentos de Janeiro de 2010 até Setembro de 2021
. Os dados do IBGE foram pegos os que são disponibilizados para o TCU, e só temos as informações anuais. Para as comparações trimestrais fiz uma interpolação linear nesses dados
### Observações sobre as Análises
Eu gosto sempre de começar as análises do macro para o micro, desta forma o primeiro notebook acaba avaliando a visão do Brasil como um todo. O segundo notebook foca numa análise comparativa por região e o terceiro foca nos estados do Sudeste, comparando-os com as regiões Sul e Nordeste. Isso porque quis confirmar uma hipótese de que os estados de São Paulo e Minas Gerais seguem comportamentos mais próximos da região Sul. Enquanto Rio de Janeiro e Espírito Santo são mais próximos do comportamento da região Nordeste.
Todas as análises foram feitas por trimestres por permitir a visão de sazonalidade, mas também reduzindo a quantidade de estimativas por interpolação da quantidade de habitantes, dado que esse dado só possuía informações anuais.
Fora isso escolhi um período de 7 anos de histórico, de 2014 até 2020. E incluí também o primeiro semestre de 2021, não inclui mais informações de 2021 porque a informação por data de atendimento é abastecida ainda por alguns meses de processamento posteriores, fazendo com que os meses finais da base de dados fiquem sempre distorcidos.
A análise possou por diversos indicadores, já o detalhamento da análise foi nos indicadores de sazonalidade de óbitos pré pandemia de covid-19 e do incremento de óbitos e gastos no período pandêmico frente ao período anterior.
### Conclusões
Nas análises conseguimos identificar que os óbitos, bem como as internações, possuem uma sazonalidade. Fora isso, ficou evidente o efeito da pandemia da covid-19 em todos os indicadores. Talvez o mais surpreendente, mas de certa foram dentro do esperado, foi o número de internações por habitante no período pandêmico que teve uma queda relevante no início, e mesmo depois não retomou patamares anteriores, porém não segui uma linha de análise desse indicador. Caso queira seguir essa análise sugiro buscar informações de internações por motivo que talvez possa auxiliar.
Com relação as análises mais detalhadas de sazonalidade de óbitos vemos uma evidência muito forte que ela está relacionada a sazonalidade das doenças respiratórias, levando em conta a informação da live do Atila Iamarino (Live 07/06 - Brasil: análise técnica da pandemia com Wanderson de Oliveira: https://www.youtube.com/watch?v=BtVZ-Gxh8dE&list=PLRRpjE6bL5UxzWZ2T7Gt6pIlFdR4ig4YX no trecho de 1h e 11min até 1h e 30min).
Essa evidência se comprova nas 3 análises, mas principalmente na por Região e na dos estados do Sudeste. Para confirmá-la sugiro buscar uma base de dados de óbitos por motivo e mês, para confirmar que as doenças respiratórias são as que fazem o total ter essa sazonalidade.
Com relação as análises da pandemia, vimos um número muito triste de perto de 300mil mortes em excesso no SUS frente aos anos anteriores no período do 2º Tri de 2020 até o 2º Tri de 2021. Mostrando que o cenário foi terrível no período.
Nas análises por região verificamos que a região Sul teve o maior aumento nominal de óbitos por habitante, uma morte a mais ao mês para cada 10 mil habitantes no período pandêmico frente aos anos anteriores, sendo a mais afetada na minha opinião. Já a região Norte teve o maior incremento percentual de mortes por habitante, que é algo preocupante e justifica os noticiários sobre o que aconteceu em Manaus principalmente.
Pela perspectiva dos estados do Sudeste o maior impacto ficou no Espírito Santo que teve o maior aumento nominal e percentual. Ele teve um aumento de 1,2 mortes a cada 10 mil habitantes ao mês, 66% maior que os anos anteriores a pandemia.
Outro dado que chamou atenção no Espírito Santo foi que ele também foi o estado do Sudeste que mais aumentou os gastos por internação, 69% ou 853 reais por internação, durante o período pandêmico. Sendo que o segundo estado nesse quesito no Sudeste foi São Paulo, que ficou bem atrás, mais próximo dos outros, com 52% de incremento, R$708.
Esse ponto dos incrementos dos gastos chama bastante atenção, ainda mais que quanto mais aumentam as mortes, maiores são os gastos por internação. Isso me deixa preocupado e querendo entender melhor o que gerou isso. 
Sei que tivemos um investimento grande em respiradores e imagino que o procedimento de intubação seja mais caro também. Porém, dada a quantidade de notícias sobre a utilização de remédios sem eficácia, bem como o superfaturamento no contrato de compra de vacinas, gera a dúvida de qual foi o real motivo desse incremento. Acredito que vale uma análise particular sobre isso com mais dados do destino dessa verba.
### Comentários finais
Não foi fácil fazer esse primeiro projeto utilizando python, sofri bastante aprendendo a linguagem, realizando as lições e este projeto ao longo dessa uma semana e meia. Acredito que com isso o storytelling possa ter ficado prejudicado.
De qualquer maneira foi interessante, acredito que o resultado foi bom e o aprendizado maior ainda.
E não podia de deixar de agradecer minha esposa e minha filhinha que me deixaram me dedicar a isso neste fim de semana.
Até a próxima!
