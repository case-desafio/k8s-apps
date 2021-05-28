# k8s-apps
Repositório que contém os manifestos para deploy das apis Stocks, Wallet, serviços de monitoria e logging.  
Api stocks busca os dados do site https://mfinance.com.br/.   
Implementado duas versões do serviço.Na primeira os dados são buscado todas vez na api externa,
demorando um certo tempo para retornar as informações, na V2 os dados são buscados uma vez e adicionados em um cache no redis.  
As informações ficam armazenadas por um determinado período, o qual pode ser configurado. A api wallet prove endpoints para criação
de usuários e registros de compra ou venda de ações, conforme código e usuário informado, calculando o custo médio das ações.  

Executar os comandos conforme orientações nos arquivos README de cada seção.
