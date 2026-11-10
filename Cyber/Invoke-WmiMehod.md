[[cmdlet]] que chama um método de uma classe ou objeto do [[WMI]] seja em uma máquina local ou em uma remota.

### Abuso

```
Invoke-WmiMethod -Class Win32_Process -Name Create -ArgumentList 'cmd.exe /c <comando>' -ComputerName <alvo>
```

**`Invoke-WmiMethod`**  
O cmdlet: executar um método WMI.

**`-Class Win32_Process`**  
A classe WMI alvo. `Win32_Process` representa os **processos** do Windows.

**`-Name Create`**  
O método a executar. `Create` da classe `Win32_Process` **cria um novo processo** na máquina alvo. É um método estático, por isso não precisa de um objeto existente.

**`-ArgumentList 'cmd.exe /c <comando>'`**  
O argumento passado ao método `Create`: a linha de comando do processo a ser criado.

- `cmd.exe` abre o prompt do Windows.
- `/c` manda executar o comando seguinte e depois encerrar.
- `<comando>` é um placeholder para o que será executado.
- As aspas simples evitam que o PowerShell interprete caracteres especiais.

**`-ComputerName <alvo>`**  
A máquina onde o método será executado. Sem esse parâmetro, roda localmente. Com ele, a chamada vai pela rede (DCOM, porta 135 mais portas dinâmicas altas) e **exige credenciais com privilégio administrativo no alvo**. Pode ser combinado com `-Credential` para informar outro usuário.

**Lendo tudo junto:** “Pelo WMI, na máquina `<alvo>`, chame o método que cria um processo e faça ele executar `cmd.exe /c <comando>`.” É, na prática, **execução remota de comandos**, parecida com o que o PsExec faz, mas usando só recursos nativos.
