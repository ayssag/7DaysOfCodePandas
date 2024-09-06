# #7DaysOfCode Python Pandas

<aside>
🔎 Um dos objetivos de uma biblioteca é garantir que os materiais informacionais estejam sendo **utilizados**. Os empréstimos realizados podem ser um indicador, mesmo que de forma básica (pois você não consegue garantir que haja uma leitura ou utilização real).

Por este motivo, entender a quantidade de empréstimos se torna importante.

Questões de diferentes perspectivas podem surgir como:

- A quantidade de empréstimos está aumentando ou diminuindo ao decorrer dos últimos anos?
- Em quais bibliotecas do sistema estão a maior quantidade de empréstimos?
- Quais são os temas mais emprestados? E os menos?

Com estas e outras informações será possível entender o cenário e apresentá-lo à diretoria das bibliotecas, para que possam tomar melhores decisões na melhoria da infraestrutura, dos recursos e processos da unidade de informação.

Mas para que tudo isso seja realizado, você precisará começar com a coleta e organização dos dados para que possa trabalhar com eles nas próximas análises.

</aside>

# Objetivo

Explorar os dados de empréstimos dos acervos do sistema de bibliotecas da UFRN.

## Perguntas

- A quantidade de empréstimos está aumentando ou diminuindo ao decorrer dos últimos anos?
- Em quais bibliotecas do sistema estão a maior quantidade de empréstimos?
- Quais são os temas mais emprestados? E os menos?

# Dia 1/7 > Importação de dados

Você trabalhará com dados apenas dos últimos 10 anos disponíveis.

## Fonte

[7_Days_of_Code_Alura-Python-Pandas/Dia_1-Importando_dados/Datasets/dados_emprestimos at main · FranciscoFoz/7_Days_of_Code_Alura-Python-Pandas](https://github.com/FranciscoFoz/7_Days_of_Code_Alura-Python-Pandas/tree/main/Dia_1-Importando_dados/Datasets/dados_emprestimos?utm_medium=email&_hsenc=p2ANqtz-9RHqRk5F67foKdFL3RWZE3CBA1JokMoVmY7JUah8KgKtSDwyLi7cZwXgMoNxY0LtQspuunbT1y93SmvySY1zjs8u4fXA&_hsmi=270874190&utm_content=270874190&utm_source=hs_automation)

## Etapas

- [x]  Importar dados dos empréstimos
- [x]  Unificar os dados de empréstimos em único Dataframe
- [x]  Importar exemplares do acervo
- [x]  Mesclar empréstimos com exemplares (relação ⇒ código de barras do exemplar)

## Dicas

<aside>
💡  Importar os dados diretamente do Github para seu notebook apenas passando o endereço do link “Raw” como origem.

</aside>

[IO tools (text, CSV, HDF5, …) — pandas 2.2.2 documentation](https://pandas.pydata.org/docs/user_guide/io.html?utm_medium=email&_hsenc=p2ANqtz-8uo58bEMbH5Z557ZPb9BrIxFKmMZz8oaeFBSzwrMTBEN8a1OTXUBSsx6pIUAvmnNEiDmsJFaP4P9LmaRM6DJj8971-lg&_hsmi=270874190&utm_content=270874190&utm_source=hs_automation)

<aside>
💡 Formato Apache Parquet

</aside>

[O que são Arquivos Parquet e quais as Vantagens? | Alura](https://www.alura.com.br/artigos/arquivos-parquet?utm_medium=email&_hsenc=p2ANqtz-8ULqeoidGzlm_nVOQT94u2NHnUxLswDsA43rZ3jhiouuao5QB-r8xffFrh_yWtgBFa1ggMmcrMqKUthVQpHbxVymSEYg&_hsmi=270874190&utm_content=270874190&utm_source=hs_automation)

[Como jogar dados fora com Pandas?](https://franciscofoz.medium.com/como-jogar-dados-fora-com-pandas-23a5be871aac)

# Dia 2/7 > Limpeza de dados

Você irá iniciar a limpeza e atribuir mais contexto aos seus dados para depois aprofundar-se nas análises.

## Etapas

- [x]  Remover dados nulos ou duplicados
- [x]  Criar uma nova coluna com os valores da localização, para refletir a respectiva classe geral na CDU
- [x]  Excluir a coluna *"registro_sistema"*, pois ela não está fazendo sentido para essa análise
- [x]  Transformar a coluna da matricula (*“matricula_ou_siape”*) em string, pois ela não está com um formato muito legível

## Dicas

<aside>
💡 CDU - Classificação Decimal Universal

- *"Os itens do acervo em uma biblioteca são organizados por um sistema de classificação de acordo com o respectivo tema. Existem diversos sistemas, mas este conjunto está de acordo com a [CDU - Classificação Decimal Universa](https://empresas.alura.com.br/e3t/Ctc/I8+113/d2z6gD04/MWLRmyXRz6xW3vBlLR5n_pZnW2z6fd_5hXVq0N3wqV7M3lYMRW7Y8-PT6lZ3q7W76GxQ93gcgtBW1lJys7602D2WW5jZlMY8FpJ_NVNHzvM5pmrhQW2yyMhD5KR156N8DcfqRDZK5-W96tysq4K9VB-W76lVz52GYgpvW3Yw6YX6vChhZW4zmmYc8XhpMvW2kfck358PST8W2m8xrs4VpMgXW9cvrQJ1R03H5W8XrD5y1tNqt9W8yv84b6Ky6JNW8dwv7P37SdTgW1JVW4460mR-XW3VcF2d7GlYHLW6X0NNJ1C-CPjN23JYbsFlGb_W8lDjCs1CmqGqW5yC8597bSbdqW1GN9tL6yqSNgW1BtyCQ7J-TXQW616gPk80wqKFW3qGwSJ7_38Rjf6L5k0-04)l. Esta classificação é decimal, pois varia de acordo com a classe de cada assunto ⬇️*
    - *000 a 099: Generalidades. Ciência e conhecimento.*
    - *100 a 199: Filosofia e psicologia.*
    - *200 a 299: Religião.*
    - *300 a 399: Ciências sociais.*
    - *400 a 499: Classe vaga. Provisoriamente não ocupada.*
    - *500 a 599: Matemática e ciências naturais.*
    - *600 a 699: Ciências aplicadas.*
    - *700 a 799: Belas artes.*
    - *800 a 899: Linguagem. Língua. Linguística.*
    - *900 a 999: Geografia. Biografia. História."*
    
    *Portanto, se um material tiver um código de localização 720, ele está dentro da classe geral de “**Belas Artes**”; ou se tiver um código 028, estará dentro da classe geral de “**Generalidades. Ciência e conhecimento**”.*
    
</aside>

# Dia 3/7 > Análise exploratória de dados e DateTime
Por isso, o empréstimo dos materiais em uma biblioteca é uma das formas de se indicar o uso da informação. Entender a quantidade e quando se emprestaram os livros é uma das primeiras formas de fazer uma análise desse tipo. A diretoria da biblioteca gostaria de entender se a quantidade de empréstimos está diminuindo, aumentando ou permanecendo igual ao decorrer dos últimos anos. A diretoria também gostaria de gerenciar melhor os recursos humanos da biblioteca de acordo com a demanda de trabalho existente, como por exemplo:
- gerenciar a programação de férias dos colaboradores de acordo com os meses de menor demanda;
- programar atividades que não sejam de atendimento ao usuário para períodos específicos de menor demanda.
Além do gerenciamento anual das atividades, a diretoria também necessita que seja planejada uma programação diária das atividades.

## Etapas
- [x] Verificar qual é a quantidade total de exemplares emprestados por cada ano e plotar um gráfico de linhas.
- [x] Fazer uma análise em relação à visualização gerada.
- [x] Gerar uma tabela com a quantidade total de exemplares emprestados por mês e descubrir quais meses são os que possuem a maior quantidade de empréstimos realizados.
- [x] Plotar um gráfico de linhas.
- [x] Trazer suas análises em relação a quais meses poderiam ser as melhores opções para férias dos colaboradores.
- [x] Verificar quais foram os horários com maior quantidade de empréstimos ao longo de um dia inteiro.
- [x] Plotar um gráfico de barras e analisar quais seriam os melhores horários para alocar as demais atividades que não sejam de atendimento ao usuário.

## Dicas

<aside>
    💡
    1. Atente-se para a quantidade de exemplares emprestados, e não de empréstimos realizados. <br>
    2. Verifique a quantidade de empréstimos pelos números de ID. <br>
    3. Investigue pela relação deles com o ID dos exemplares. <br>
    4. O groupby poderá te ajudar nesse desafio. <br>
    5. Transforme as datas em tipo Datetime. <br>
</aside>

# Dia 4/7 > Análise exploratória de dados e Variáveis
O objetivo será entender a quantidade de empréstimos a partir das variáveis categóricas do seu conjunto de dados. Vamos explorar algumas das variáveis categóricas das quais precisaremos extrair mais informações. Elas são:
- Tipo de vínculo
- Coleção
- Biblioteca
- Classificação geral da CDU

Para explorar os dados, alguns questionamentos serão pertinentes para a diretoria das bibliotecas, como:
- <em>“Como se distribuem os empréstimos de exemplares pelos tipos de vínculo dos usuários?”</em>
Desta forma, a diretoria poderá entender qual é o público que está utilizando a biblioteca e assim tomar decisões em continuar com a estratégia de negócio atual ou modificá-la.

- Quais coleções são mais emprestadas?
Da mesma forma, as coleções. Ranquear as coleções mais emprestadas pelo público, será bastante importante para a estratégia atual.

- Quais são as bibliotecas com mais ou menos quantidade de empréstimos?
Assim, a diretoria conseguirá entender onde ela deverá melhorar e focar suas iniciativas.

## Etapas
- [x] Gerar uma tabela de frequência e com o percentual para cada variável.
- [ ] Trazer algumas das suas percepções para as análises com o que você poderá contribuir para a diretoria da biblioteca.
- [ ] Apontar algumas outras métricas que poderiam entrar aqui para enriquecer essa análise.
<em>"De quais temas da CDU são os exemplares emprestados?"</em>
Entender quais os temas mais procurados pelos usuários é fundamental para o desenvolvimento de novos planos de marketing do acervo. Para que possam não apenas fortalecer o que está sendo utilizado, mas também promover o que não está.

## Dicas
<aside>
    1. Como é um trabalho repetitivo, crie uma função que gere a tabela com os valores. <br>
    2. Para arredondar os números do percentual, você pode utilizar a função built-in do Python Round(). <br>
</aside>

# Dia 5/7 > Análise exploratória de dados e Boxplot
O Boxplot é uma das visualizações mais poderosas que existe, pois ele permite que você visualize medidas estatísticas como a mediana, os quartis, os valores mínimos e máximos e os valores atípicos outliers. 
![image](https://github.com/user-attachments/assets/ee56f0fb-1cb4-44ae-b7a3-eea43279cab2)

É importante realizar avaliações constantes do uso da biblioteca e entender em quais cenários (tipos de usuários, estratégias de marketing, atualização de acervo, cenário sócio-político interno e externo) é melhor manter a estratégia atual ou mudá-la. Você vai fazer dois recortes em seus dados para entender como eles se distribuíram ao decorrer desses anos e, desta forma, possa trazer inferências para levar à diretoria da biblioteca, a fim de que eles possam tomar decisões para o ano atual. Você vai avaliar dentre os alunos de graduação e pós graduação a distribuição de empréstimos mensais por ano realizados entre 2010 e 2020 da coleção que tiver a maior frequência de empréstimos.

## Etapas
- [x] Plotar um gráfico para cada tipo de usuário.Tenha um boxplots para cada ano.
- [ ] Analisar o que ocorreu.
<aside>
    <em>
        "O que está ocorrendo ao decorrer do tempo?" <br>
        "Houve algum ano ou anos em específico que te chamaram atenção para alguma diferença?" <br>
        "Quais as maiores diferenças entre os empréstimos para os alunos de graduação e pós graduação?" <br>
    </em>
</aside>

## Dicas
<aside>
    💡 Desenvolva a tarefa uma etapa por vez: <br>
    1. Verifique qual é a coleção com maior frequência para cada tipo de usuário.<br>
    2. Filtre os dados com condições solicitadas <br>
    3. Selecione apenas os empréstimos <br>
    4. Faça a contagem de empréstimos mensais por cada ano <br>
    5. Crie uma função para gerar a visualização do gráfico de box plot por cada ano. <br>
    6. Crie o gráfico de boxplot <br>
</aside>
<hr>
<aside>
    💡 Bibliotecas para plotar os gráficos <br>
    - Matplotlib <br>
    - Pandas <br>
    - Seaborn <br>
    - Plotly <br>
</aside>

# Dia 6/7 > JSON, Excel e Pivot_table
As instituições de ensino superior (IES) têm a necessidade de passar por avaliações do Ministério da Educação (MEC) para que possam ofertar e continuar ofertando cursos de graduação e pós-graduação. A biblioteca universitária faz parte de um dos indicadores da avaliação dos cursos, em principalmente três aspectos: acervo, infraestrutura e serviços. Os cursos serão:
- Biblioteconomia
- Ciências sociais
- Comunicação social
- Direito
- Filosofia
- Pedagogia
A universidade forneceu os dados dos usuários, mas uma parte deles está em planilhas de Excel, a outra parte veio através de uma API do sistema em formato JSON.

## Etapas
- [x] Extrair os dados destes arquivos, agrupe-os em apenas um só, e verifique depois a quantidade de empréstimos.
- [x] Calcular a quantidade de empréstimos realizados entre 2015 e 2020 por cada curso de graduação que passará pela avaliação.
- [x] Gerar uma tabela com as seguintes características:
- Índice: Cursos
- Colunas: Ano
- Valores: Quantidade de empréstimos
- Total: Acrescente uma linha e uma coluna de total a tabela



