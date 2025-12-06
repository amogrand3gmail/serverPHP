# README

## Visão geral

Script PHP version 8.4 simples que executa o servidor embutido (PHP -S) em segundo plano. 
O script recebe comandos via linha de comando: "on" para iniciar o servidor e "off" para parar. 

Ele usa um arquivo de JSON para gerenciar o processo do servidor.

Observações:
- O servidor embutido é adequado para desenvolvimento, não para produção.
- O script assume que o PHP está disponível no PATH como php.
- Substitua localhost e 8090 conforme necessário.
- O script usa PID para permitir start, stop e kill do processo.

Contempla autoload manual em PHP com duas classes: `Base` e `Serve`. O autoload registra uma função anônima para incluir arquivos de classe com base no namespace/class name. O código demonstra a criação de objetos e a leitura de seus atributos.

## Observações técnicas

**Autoload básico**:
 - O autoload utiliza `spl_autoload_register` para incluir arquivos com base no nome da classe.
 - A convenção usada é que o nome da classe corresponde ao nome do arquivo (ex.: `Base` -> `Base.php`).
   
## Estrutura de Arquivos

├── App

│   ├── Base.php

│   ├── config.json

│   ├── index.php

│   ├── public

│   │   └── index.php

│   ├── Serve.php

│   ├── server.log

│   └── servidor.php

└── readme.md