# ApiCrawler

Api que recebe uma lista de URLS e um termo a ser pesquisado seguindo o formato:

`http://127.0.0.1:5000/findword?array=[url1,url2]&word=termo_a_pesquisar`

Api utiliza Quart como base, uma versão assíncrona do Flask, e Pytest para os testes.

## Deploy
Instalação do Pip para python 3 no linux

`sudo apt-get install python3-pip`

A instalação do Python 3 no Windows já vem com o pip3.

Instalação do quart para python 3

`pip3 install quart`

Instalação do aiohttp para python 3
`pip3 install aiohttp`

Exportar e rodar a aplicação
### Linux
`export QUART_APP=QuartApiAssincrona.py`

`quart run`

### Windows
`set QUART_APP=QuartApiAssincrona.py`

`quart run`

Basta usar a url passando os parâmetros

`http://127.0.0.1:5000/findword?urls=[url1,url2]&termo=termo_a_pesquisar`

## Parâmetros
### Obrigatórios
* urls: É a lista de urls que serão utilizadas para busca do termo
* termo: É o termo que vai ser pesquisado nos sites enviados
### Opcional
* ignorecache: Define se o cache em disco será utilizado (False) ou ignorado e os dados baixados novamente (True)

### Exemplo com todos os parâmetros
`http://127.0.0.1:5000/findword?urls=['https://techcrunch.com/', 'canaltech.com.br']&termo=google&ignorecache=True`

## Testes
Instalação Pytest

`pip3 install -U pytest`

Rodar o comando pytest na pasta

`pytest`
