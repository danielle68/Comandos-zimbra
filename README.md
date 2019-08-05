# Comandos-zimbra

==> Comandos devem ser utilizados como o usuário Zimbra

## sudo su - zimbra

==>Listas Quotas dos usuários
## zmprov gqu `hostname`  | awk {'print " "$3/1048576" "$2/1048576" "$1'}

==> Criar novo usuário
## zmprov ca exemplo@secnet.com.br senha displayName 'Joao da Silva'

==> Exportar Emails (Caixa/Mailbox)
## zmmailbox -z -m exemplo@secnet.com.br getRestURL "//?fmt=tgz"> /tmp/exemplo-secnet.com.br.tgz

==> Importar Emails (Caixa/Mailbox)

==> APAGA OS DADOS NO DESTINO
## /opt/zimbra/bin/zmmailbox -z -m exemplo@secnet.com.br postRestURL “//?fmt=tgz&resolve=reset” /tmp/exemplo-secnet.com.br.tgz

==> MESCLA OS DADOS NO DESTINO
## /opt/zimbra/bin/zmmailbox -z -m exemplo@secnet.com.br postRestURL “//?fmt=tgz&resolve=modify” /tmp/exemplo-secnet.com.br.tgz

==> Alterar senha de administrador do painel de administração
## zmprov sp administrador@secnet.com.br novasenha

==> Ativa Acesso HTTP e HTTPs no servidor
## /opt/zimbra/bin/zmtlsctl mixed
## zmcontrol restart

* Referências:
==> links:https://www.secnet.com.br/clientes/knowledgebase/75/Comandos-Zimbra.html
==> links:
