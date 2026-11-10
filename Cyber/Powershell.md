Segunda principal forma de executar programas no Windows, veio de forma a substituir o cmd, pois é bem mais avançado e permite várias outras funcionalidades

### Característica

Diferentemente do cmd que chama outros programas e passa os argumentos o Powershell não tem essa finalidade, ele não cria processos, ele executa cmdlets dentro do espaço do seu próprio processo, ou seja tende a gastar menos memória.

### Abuso
Por não criar processos para cada ação tomada é possível para atacantes realizarem diversas operações no Powershell sem alertar ferramentas de defesa que monitoram criação de processos.

### Prevenção
A principal forma de se monitorar o Powershell é por meio do Event Id [[4104]], este que vai gravar toda e qualuqer coisa que for executada dentro do powershell, mesmo comandos codificados depois de sua decodificação;

### Argumentos

- `-Command (-c)`: Executa o que vem a seguir
- `-File`: Roda um arquivo .ps1
-  `-EncodedCommand`: Recebe comando em [[Base64]], muito usado de forma maliciosa
-  `"..."`: Agrupa tudo em um único argumento