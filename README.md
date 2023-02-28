# 1. - Introdução

<hr>

## 1.1 - Sobre o Polars

Este tutorial é destinado àqueles que desejam aprender mais sobre Polars. Ao invés de ter uma abordagem teórica massante, vamos fazer exemplos práticos para te apresentar as principais funcionalidades do Polars. Não vou colocar todas para não lotar o seu cérebro de informação. Se quiser saber todas as funções, leia a documentação oficial <a href="https://pola-rs.github.io/polars/py-polars/html/reference/index.html" target="_blank">clicando aqui</a>. 

Antes de iniciar, é muito importante você saber o que é o Polars e o porquê você está aprendendo ele. Sendo assim, vamos discutir mais sobre essa biblioteca que está sendo tão falada no meio de Data Science.

A seguir, algumas informações sobre o Polars:
<ul>
    <li> Utiliza todos os núcleos disponíveis da sua máquina;
    <li> Otimiza queries para reduzir alocações de memória/trabalho desnecessárias; 
    <li> Consegue lidar com datasets muito maiores que sua RAM disponível;
    <li> Tem uma API consistente e previsível;
    <li> Os datatypes devem ser conhecidos antes de executar a query. 
</ul>

<hr>

## 1.2 - Performance

O polars é extremamente rápido, e, atualmente, é uma das bibliotecas com a melhor performance disponível. Por ser desenvolvido em Rust, ele possui a performance de C/C++. Observe, a seguir, uma comparação da velocidade:


  <img src="https://i.ibb.co/bB5Kkw8/0-2n0-Wx-R2qvc1z5f-Mg.png">
<ul>
    <li><a href = "https://github.com/pola-rs/tpch" source = "_blank">Link da imagem original</a>
</ul>

No eixo y, temos o tempo em segundos para a execução de 5 bibliotecas diferentes: Polars, Pandas, Dask, Modin e Vaex. No gráfico, a barra roxa representa o Polars. No eixo x, temos 7 queries diferentes. Note que, em todas as queries, o Polars obteve um desempenho muito superior quando comparado às outras bibliotecas.

<br>

Agora que tivemos uma breve apresentação, vamos aos códigos!

<hr>

## 1.3 - Mais informações sobre o dataset

Esse dataset fornece informações de clientes de uma empresa automobilística. Em seu mercado existente, a equipe de vendas classificou todos os clientes em 4 segmentos (A, B, C, D). 

A seguir, um breve resumo sobre as variáveis do dataset:

<ul>
    <li> <strong>ID</strong>: ID único do cliente
    <li> <strong>Gender</strong>: Gênero (Male: Homem, Female: Mulher)
    <li> <strong>Ever_Married</strong>: Já casou? (True: Verdadeiro, False: Falso)
    <li> <strong>Age</strong>: Idade
    <li> <strong>Graduated</strong>: É graduado? (True: Verdadeiro, False: Falso)
    <li> <strong>Profession</strong>: Profissão
    <li> <strong>Work_Experience</strong>: Anos de experiência no trabalho
    <li> <strong>Spending_Score</strong>: Score dado ao cliente baseado em quanto ele gastou na loja e em seu comportamento (Low: Baixo, Average: Médio, High: Alto)
    <li> <strong>Family_Size</strong>: Tamanho da família 
    <li> <strong>Var_1</strong>: Variável anônima 
    <li> <strong>Segmentation</strong>: Segmento ao qual o cliente pertence
</ul>
