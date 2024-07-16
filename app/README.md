# Autores:
* [Mário Minhava](https://github.com/Mariola04)
* [Francisco Tavares](https://github.com/kikotavares10)
* [Francisco Carqueija](https://github.com/kikokite)


# Contexto
Projeto desenvolvido no âmbito da cadeira de Base de Dados que consistia no desenvolvimento de um website com ligações a uma base de dados à nossa escolha usando flask.
A base de dados escolhida foi de jogos de xadrez da plataforma lichess.org 
Inúmeras entradas foram adicionadas manualmente como Win Rate dos jogadores ou mesmo a nacionalidade

# Desenvolvimento da aplicação da 2ª parte do projeto

A primeira parte deste projeto foi anteriormente desenvolvida e consistia no desenho de um diagrama de classes UML e um diagrama ER para a nossa base de dados, o nosso projeto tem por base esses diagramas e todas as ligações aí criadas

## Instalação de software

Precisa de ter o Python 3 e o gestor de pacotes pip instalado.
Experimente executar `python3 --version` e `pip3 --version` para saber
se já estão instalados. Em caso negativo, pode por exemplo em Ubuntu
executar:

```
sudo apt-get install python3 python3-pip
```

Tendo Python 3 e pip instalados, deve instalar a biblioteca `Flask` executando o comando:

```
pip3 install --user Flask
``` 

## Configuração de acesso à BD

Edite o ficheiro `db.py` no que se refere à configuração da sua BD, modificando os parâmetros `DB_FILE` que indique o ficheiro da base de dados. O ficheiro SQLite para a BD deve residir na mesma pasta que o ficheiro `app.py`.

Configurados o parâmetro `DB_FILE`,  teste o acesso executando:

```
python3 test_db_connection.py NOME_DE_UMA_TABELA
```

Se a configuração do acesso à BD estiver correcto, deverá ser listado o conteúdo da tabela `NOME_DE_UMA_TABELA`, por ex. se a BD configurada fosse a dos recintos culturais e quisermos listar a tabela `atividades` obteríamos:

```
$ python3 test_db_connection.py atividades
6 results ...
[('ref', 1), ('atividade', 'cinema')]
[('ref', 2), ('atividade', 'circo')]
[('ref', 3), ('atividade', 'dança')]
[('ref', 4), ('atividade', 'música')]
[('ref', 5), ('atividade', 'tauromaquia')]
[('ref', 6), ('atividade', 'teatro')]
```

## Execução do servidor da aplicação

Depois de configurar a BD como descrito acima, pode agora iniciar o servidor da aplicação executando `python3 server.py`, ex.:

```
$ python3 server.py
2021-05-18 21:40:46 - INFO - Connected to database guest
 * Serving Flask app "app" (lazy loading)
 * Environment: production
   WARNING: This is a development server.  Do not use it in a production deployment.
   Use a production WSGI server instead.
 * Debug mode: off
2021-12-08 21:40:46 - INFO -  * Running on http://0.0.0.0:9000/ (Press CTRL+C to quit) 
...
```

De seguida abra no seu browser __http://127.0.0.1:9000__ ou __http://localhost:9000__. Deverá ver uma página com o nosso website.

## Mais referências

- HTML: 
   - [W3 schools tutorial simples](https://www.w3schools.com/html/default.asp)
   - [referência Mozilla](https://developer.mozilla.org/en-US/docs/Web/HTML) 
- Bibliotecas:
  - [sqlite3](https://docs.python.org/3/library/sqlite3.html)
  - [Flask](https://flask.palletsprojects.com/en/1.1.x/)
  - [Jinja templates](https://jinja.palletsprojects.com/en/2.10.x/templates/)

