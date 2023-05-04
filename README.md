# Sistemas - Appia Nansen Integration

Alguns pontos do projeto

* Desenvolvido em python
* Independência de módulos
* Escalável

Requisitos

* Python 3.9.x ou superior
* Banco de dados MySQL (dump contido no arquivo IoDAnansencas.sql na pasta raíz do projeto)

Passos para a execução

* Na pasta appia-json, executar o comando pip install -r requirements.txt para instalar as dependências utilizadas no projeto.
* Também na pasta appia-json, realizar as alterações necessárias no arquivo configuration.ini. As configurações serão explicadas com mais detalhes na próxima seção.
* Na pasta appia_json executar o comando:
  - python main.py normal, caso deseje executar a aplicação normalmente em primeiro plano, com visualização de logs em tempo real
  - python main.py daemon, caso deseje executar a aplicação em segundo plano, como um serviço do sistema operacional.


Configurações do arquivo configuration.ini

* [mysql]

  - host = host do serviço de banco de dados utilizado
  - port = porta do serviço de banco de dados utilizado
  - user = nome de usuário do banco de dados utilizado
  - passwd = senha do banco de dados utilizado
  - db = nome do banco de dados utilizado

* [hemera]

  - ip = endereço da aplicação Hemera utilizada
  - port = porta da aplicação Hemera utilizada
  
[sanplat]

  - base_url = endereço da aplicação Sanplat utilizada
  - login_url = rota de login da aplicação Sanplat utilizada
  - meter_read_url = rota de leitura do medidor da aplicação Sanplat utilizada
  - read_channel_url = rota de leitura de canais da aplicação Sanplat utilizada
  - meter_set_url = rota de configurações de medidor da aplicação Sanplat utilizada
  - tariff_set_url = rota de comandos relacionados a tarifas da aplicação Sanplat utilizada
  - remote_url = rota de conexão/desconexão de medidores da aplicação Sanplat utilizada
  - user = usuário da aplicação Sanplat utilizada
  - passwd = senha da aplicação Sanplat utilizada

* [prometheus]

  - port = porta da aplicação Prometheus utilizada (opcional, coleta dados de estatística em tempo real)
  
* [fastapi]

  - host = host utilizada pela API Sanplat-Hemera (utilizada para cadastro em massa de dispositivos no banco de dados)
  - port = porta utilizada pela API Sanplat-Hemera
  
* [device]

  - serial_test = serial do dispositivo utilizado como teste
