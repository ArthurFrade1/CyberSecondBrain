LOLBin reponsável por gerenciar usuários, grupos, compartilhamentos, serviços e conexões de rede. Fica em `C:\Windows\System32\net.exe`
### Subcomandos principais

|Subcomando|Função|Exemplo|
|---|---|---|
|`net user`|Lista, cria, altera ou apaga contas de usuário|`net user` / `net user joao Senha123 /add`|
|`net localgroup`|Gerencia grupos locais e seus membros|`net localgroup Administrators`|
|`net group`|O mesmo, mas para grupos de domínio (Active Directory)|`net group "Domain Admins" /domain`|
|`net share`|Cria e lista pastas compartilhadas|`net share`|
|`net use`|Conecta a um compartilhamento de rede|`net use Z: \\servidor\pasta`|
|`net view`|Lista computadores e compartilhamentos na rede|`net view \\servidor`|
|`net start` / `net stop`|Inicia ou para serviços|`net stop spooler`|
|`net accounts`|Política de senhas e bloqueio|`net accounts`|
|`net session`|Sessões remotas abertas na máquina|`net session`|
|`net time`|Hora de outra máquina|`net time \\servidor`|