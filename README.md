# develdocs

## Efetuar Login  

### - Logging 
- Para efetuar login em um server, o usuário precisa fornecer o endereço do server ao qual deseja se conectar e o seu nickname de jogador:

  |Argumento |Tipo   |Descrição                                                 |
  |----------|-------|----------------------------------------------------------|
  |Endereço  |String |Endereço no qual existe um servidor esperando por conexões|
  |Nick      |String |Nick que o usuário vai usar para jogar                    | 
  |Team      |Stirng |Equipe do jogador (Cliente Gtetrinet)                     |

### - Encoded login message from client to server
- O cliente deve fazer o encode da mensagem e enviar os seguintes dados em uma string:

  |Argumento      |Tipo   |Descrição                                                 |
  |---------------|-------|----------------------------------------------------------|
  |Tetris start   |String |Comando para iniciar conexão                              |
  |Nick           |String |Nick que o usuário forneceu                               |
  |Client Version |String |O número da versão da aplicação cliente                   |
  
### - Decoded login message from server to client
- O server vai fazer o decode da mensagem de login e vai responder ao cliente com as seguintes mensagens:

  ```
  playernum <number>
  ```
  
  |Argumento |Tipo   |Valores|Descrição                                                 |
  |----------|-------|-------|----------------------------------------------------------|
  |Number    |Int    |1 - 6  |Número de jogador para o novo cliente.                    |
  
  
  ```
  winlist <type><name>;<score> <type><name>;<score> ... <type><name>;<score>
  ```
  
  |Argumento |Tipo   |Valores|Descrição                                                 |
  |----------|-------|-------|----------------------------------------------------------|
  |Type      |Char   |t ou c |Especifica se a entrada é uma equipe (t) ou um jogador (p)|
  |Name      |String |       |O nome do jogador ou da equipe                            |
  |Score     |Int    |       |O score do jogador ou da equipe                           |
  
  
### - Player Team
- Recebido o playernum e winlist, o cliente enviará a mensagem setando a equipe do jogador:

  ```
  team <number> <team name>
  ```
### - Diagrama de sequência

 ![](https://github.com/rodrigaobt/develdocs/blob/master/login.svg)

  




