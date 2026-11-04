







### Funcionamento
Usa o [[APPB.dll]] combinada com [[COM Elevation]] para forçar componenetes autorizados a interagir com o [[Chrome]] por ele, conseguindo cortornar a criptografia do [[App-Bound Encryption]] sem disparar alarmes óbvios.

Usa o [[HVNC]] para criar uma área de trabalho fantasma, rodando nos bastidores invisíveis do Windows, assim o atacante consegue abrir o navegador dentro desse espaço oculto, fazer o que quiser, mesmo com a vítima logada no mesmo momento.

Usa o [[Target.dll]] para gerir a sessão do [[HVNC]], cria um desvio invisível(hook): quando o navegador fanstasma do atacante tenta aceder aos arquivos do perfil, a Target.dll redireciona esse acesso para o perfil clonado da vítima, assim fazendo com que o navegador fantasma abra já logado nas contas da vítima.