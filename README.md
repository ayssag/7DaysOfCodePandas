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