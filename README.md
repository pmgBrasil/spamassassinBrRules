# spamassassinBrRules
Regras para o spamassassin em português do Brasil

## 1 - Clone o projeto:

``cd ~/``

```git clone https://github.com/pmgBrasil/spamassassinBrRules.git```

``cd spamassassinBrRules/``

## 2 - Faça o backup do arquivo atual
``cp /etc/mail/spamassassin/custom.cf /etc/mail/spamassassin/custom.cf-bkp-`date +%Y-%m-%d-%H%M`.old``

## 3 - Copie o novo arquivo para o custom.cf
``cp spamassassin-custom.cf /etc/mail/spamassassin/custom.cf``

## 4 - Sincronize as configurações e reinicie os serviços do pmg
``pmgconfig sync --restart 1``

``systemctl restart pmg-smtp-filter pmgpolicy postfix``

## 5 - Atualizar o arquivo de regras

``cd ~/spamassassinBrRule``

``git pull``

Se houver atualizações, realize os passos 2,3 e 4 novamente
