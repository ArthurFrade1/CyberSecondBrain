Utilitário de linha de comando do Windows para se ler, criar, alterar, exportar e apagar chaves e valores do registro.

Exemplo de uso para habilitar o RDP:
`reg add "HKLM\SYSTEM\CurrentControlSet\Control\Terminal Server" /v fDenyTSConnections /t REG_DWORD /d 0 /f `
#### Explicação

- **`reg add`**: adiciona ou altera um valor no registro.
- **`HKLM\SYSTEM\CurrentControlSet\Control\Terminal Server`**: chave que guarda as configurações dos Serviços de Terminal.
- **`/v fDenyTSConnections`**: o valor a alterar (_f_ de flag, _Deny TS Connections_, “negar conexões de Terminal Services”).
- **`/t REG_DWORD`**: tipo do dado (inteiro de 32 bits).
- **`/d 0`**: o dado. Por lógica invertida, `0` significa “**não** negar”, ou seja, RDP **permitido**. Com `1`, o RDP fica desabilitado.
- **`/f`**: _force_, sobrescreve sem pedir confirmação.