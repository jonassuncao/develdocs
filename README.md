# develdocs

## Efetuar Login  

### - Logging 
- Para efetuar login em um server, o usuário precisa fornecer o endereço do server ao qual deseja se conectar e o seu nickname de jogador:

  |Argumento |Tipo   |Descrição                                                 |
  |----------|-------|----------------------------------------------------------|
  |Endereço  |String |Endereço no qual existe um servidor esperando por conexões|
  |Nick      |String |Nick que o usuário vai usar para jogar                    |  

### - Encode
- O cliente deve fazer o encode da mensagem e enviar os seguintes dados em uma string:

  |Argumento      |Tipo   |Descrição                                                 |
  |---------------|-------|----------------------------------------------------------|
  |Tetris start   |String |Comando para iniciar conexão                              |
  |Nick           |String |Nick que o usuário forneceu                               |
  |Client Version |String |O número da versão da aplicação cliente                   |
  
### - Decode
- O server vai fazer o decode da mensagem de login e vai responder ao cliente com as seguintes mensagens:

  ```
  playernum <number>
  ```
  ```
  winlist <type><name>;<score> <type><name>;<score> ... <type><name>;<score>
  ```





