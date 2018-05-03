JSON++
======

O arquivo json.py implementa um parser completo de JSON. Modifique este arquivo
para incorporar as seguintes modificações à linguagem (chamamos de JSON++):

Deve aceitar comentários no formato ``// comentário``::

  {
    // comentário!
    "foo": "bar"
  }


As vírgulas são opcionais. JSON++ deve aceitar uma vírgula após o último 
elemento de um array ou objeto::

  {
    "array": [1 2 3]
    "object": {
      "name": "John",
      "band": "Beatles, 
    }
  }


As chaves dos objetos podem ser nomes de variáveis. Nomes de variávies 
começam com uma letra e seguem com uma sequência de letras, números, hífens,
e underscores::

  {
    name: "John"
    band: "Beatles"
  }  


Aceita valores do tipo data no formato AAAA-MM-DD::

  {
    name: "John"
    band: "Beatles"
    born: 1940-10-09
  }  

Dica: use a função date(year, month, day) do módulo datetime para representar
uma data. Datas que fogem deste formato são inválidas (ex: 2000-1-1 é inválida
porque tanto o mê quanto o dia precisam de 2 dígitos)


Rodando os testes
-----------------

Rode os testes com ``pytest tests.py``. A nota é o número de testes 
que passaram - 1.

Dicas
.....

Python padrão é o Python 2:
  ``python3 -m pytest tests.py``
Para limitar a saída do pytest ao primeiro erro: 
  ``pytest tests.py --maxfail=1``
Processar um arquivo: 
  ``python3 json_plus.py ARQUIVO``
Instalar dependências:
  ``pip3 install ox-parser pytest --user -U``
Problemas com o Python 3.5?:
  ``pip3 install sidekick==0.1.0``
