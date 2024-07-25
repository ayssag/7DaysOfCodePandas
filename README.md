# #7DaysOfCode Python Pandas

> Um dos objetivos de uma biblioteca é garantir que os materiais informacionais estejam sendo **utilizados**. Os empréstimos realizados podem ser um indicador, mesmo que de forma básica (pois você não consegue garantir que haja uma leitura ou utilização real).
> 
> 
> Por este motivo, entender a quantidade de empréstimos se torna importante.
> 
> Questões de diferentes perspectivas podem surgir como:
> 
> - A quantidade de empréstimos está aumentando ou diminuindo ao decorrer dos últimos anos?
> - Em quais bibliotecas do sistema estão a maior quantidade de empréstimos?
> - Quais são os temas mais emprestados? E os menos?
> 
> Com estas e outras informações será possível entender o cenário e apresentá-lo à diretoria das bibliotecas, para que possam tomar melhores decisões na melhoria da infraestrutura, dos recursos e processos da unidade de informação.
> 
> Mas para que tudo isso seja realizado, você precisará começar com a coleta e organização dos dados para que possa trabalhar com eles nas próximas análises.
> 

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
- [ ]  Fazer a limpeza dos dados

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