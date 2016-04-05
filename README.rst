Paperboy
========

Utilitário para envio de dados de sites locais SciELO para servidores SciELO.

Como instalar
=============

pip install scielo-paperboy

Como utilizar
=============

Com arquivo de configuração
---------------------------

Criar um arquivo de configuração utilizando o template config.ini-TEMPLATE

config.ini::

    [app:main]
    source_dir=/var/www/scielo
    cisis_dir=/var/www/scielo/proc/cisis
    scilista=/var/www/scielo/serial/scilista.lst
    destiny_dir=/var/www/scielo
    ssh_server=localhost
    ssh_port=22
    ssh_user=anonymous
    ssh_password=anonymous

Criar variável de ambiente indicando o arquivo de configuração

**Linux**

    export PAPERBOY_SETTINGS_FILE=config.ini

**Windows**

    set PAPERBOY_SETTINGS_FILE=config.ini

Executar

    paperboy

Para ajuda

    paperboy --help

Para ativar módulo de compatibilidade de bases. O modulo de compatibilidade
converte as bases de dados para que sejam compatíveis com o sistema operacional
de destino. Deve ser utilizado quando o objetivo é enviar bases do Windows para
o Linux ou o contrário.

    paperboy -m

Sem arquivo de configuração
---------------------------

Executar

    paperboy --help