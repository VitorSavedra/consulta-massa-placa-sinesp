# Consulta de Placas - Sinesp
Script PHP que realiza consulta em massa de placas no Sinesp - Sistema Nacional de Informações de Segurança Pública (http://sinesp.gov.br).

### Requisitos:
- PHP 5.4 ou superior;
- cURL;
- libxml / XML.

### Como usar:
  - Clone este repositório:
    ```sh
    $ git clone https://github.com/VitorSavedra/consultaPlacaSinesp.git
    ```
  - Instale as dependências:
    ```sh
    $ composer install
    ```
  - Insira as placas a serem consultas em 'raw_file.txt', separadas por linha;
  - Execute 'getVehicleFromFile.php':
    ```sh
    $ php getVehiclesFromFile.php
    ```

### Funcionamento: 
Após executar o script, os resultados serão exibidos no terminal e salvos em dois arquivos, onde:

- bad_file.csv - Resultados de placas **não** encontradas;
- good_file.csv - Resultados de placas encontradas.

### Limites:
Não encontrei em qualquer site e nem mesmo obtive resposta do Sinesp quanto à limites na API. Na prática, encontrei bloqueios após ~60 requisições por minuto.

### Agradecimentos:
Agradecimentos ao @chapeupreto, @victor-torres e seus contribuidores por disponibilizar as APIs necessárias para este script.