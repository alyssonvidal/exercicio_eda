# Problema

<center><img src="/banner.jpg" alt="banner" width="400" height="320"/></center>

O dataset disponibilizado é de uma empresa ficticia do ramo de venda produtos eletônicos num determinado periodo. O objetivo deste desafio está em responder as perguntas abaixo.

### Perguntas

    P1: Qual horário temos mais vendas? 

    P2: Qual a marca tem o maior faturamento? 

    P3: Qual mês temos o maior faturamento?

    P4: Qual o número de clientes únicos do 3º trimestre de 2020 e qual a variação entre o 1º e 4º trimestre? 

    P5: Qual mês obteve o maior ticket médio e quanto esse resultado é maior que a média total de 2020. 

    P6: Qual produto obteve maior participação de vendas no 2º semestre de 2020? 

    P7: Quais são os top 5 produtos de maior venda 2020?


### Bonus: 

    P9: Qual tipo de informação você considera importante para compor uma análise de cliente? 

    P10: Com base nesse dataset, qual sugestão de análise ou visualização adicional você recomendaria? 



# Glossário 
| **Variavel**            | **Tipo**    | **Descrição**                                              |
| :-------------------------- | :---------- | :----------------------------------------------------------- |
| event_time                         | datatime       | Data e Hora detalhada em que a compra efetivada. |
| order_id                      | Integer     | Identificador unico do pedido.                                            |
| product_id                       | Integer | Identificador unico do produto.               |
| category_id       | Integer     | Identificador unico da categoria do produto.                        |
| category_code            | Object | Descrição resumida da categoria do produto. |
| brand       | Object     | Marca do produto.                             |
| price       | Float     | Valor do produto.                             |
| user_id       | Integer     | Identificador unico do usuário.                             |

# Desevolvimento

O projeto foi desenvolvido tanto em python quanto PowerBI. No python foi feito o tratamento de dados mais e a analise exploratória de dados, enquanto no BI foi feito a apresentação em dashboard. Importante ressaltar que independente da ferramenta os resultados tem que ser os mesmo, este foi um ponto que foi concluido com exito nesse projeto.

Apresentação: [Python](https://github.com/alyssonvidal/exercicio_eda/blob/main/exercicio.ipynb)<br>
Apresentação: [PowerBI](https://app.powerbi.com/view?r=eyJrIjoiOWViZmMwZTktMjdlYS00YTM3LWE4NjEtN2M0ODc4YjYyMzk3IiwidCI6ImQyZGYwZGI4LTM3MmYtNDExZS1iOTQ1LWRlYzRjZTU3MWI4NSJ9)


## Tratamento de Dados (Resumo)

- O dataset possuí registro de vendas de 2020 e 1970. Os registros de 1970 foram desconsiderados, por não representarem um situação real.
- Foram encontradas ordem de pedidos duplicadas. Neste caso foi mantida apenas a ultima.
- Foram encontados dados faltantes nas colunas, "price" e "user_id". Esses valores foram mantidos, no entanto isso impossibilita que algumas analises sejam precisas.
- Para facilitar a analise referente ao horario, foi criado uma nova coluna, "time" com horarios  agrupados de 15 em 15min.

<hr>

## Respostas (Resumo)

**P1: Qual horário temos mais vendas?**

10:30 com 40691 vendas

**P2: Qual a marca tem o maior faturamento?**

Samsung, com $53.831.519.49, o que representa 26.07% do faturamento da empresa

**P3: Qual mês temos o maior faturamento?**

Agosto com $36.902.067,04

**P4: Qual o número de clientes únicos do 3º trimestre de 2020 e qual a variação entre o 1º e 4º trimestre?** 

69705 unicos com variação percentual de -92,90% e -70,35% respectivamente

**P5: Qual mês obteve o maior ticket médio e quanto esse resultado é maior que a média total de 2020.**

Agosto com $217,70 e a média anual é 35,50% maior que a média anual de 2020

**P6: Qual produto obteve maior participação de vendas no 2º semestre de 2020?**

O produto "1515966223523303310" com 8277 participações

**P7: Quais são os top 5 produtos de maior venda 2020?**

Os produtos: "1515966223523303302", "1515966223523303301", "1515966223523303308", "1515966223523303310", "1515966223523303314

**P9: Qual tipo de informação você considera importante para compor uma análise de cliente?** 

- Ticket Médio do cliente
- Frequencia com que o cliente realiza as compras
- Recencia entre as compras (principalmente a ultima) realizadas pelo cliente
- Quantidade de produtos unicos que o cliente compra
- Quantidade total de produtos que o cliente compra
- Produto(s) mais caro(s) adquirido pelo cliente
- Avaliações dos clientes sobre os produtos, experiencia de compra, etc
- Preferencia de forma de pagamento
- Participações em programas de fidelidade


**P10: Com base nesse dataset, qual sugestão de análise ou visualização adicional você recomendaria?** 

- Quais categorias mais vendidas e quantas categorias unicas possui o dataset?
- Quantos produtos unicos possuem cada uma das categorias?
- Qual a porcentagem do faturamento representa cada categoria
- Qual o valor maximo de uma unica em 2020? E em cada mês?
- Cohort