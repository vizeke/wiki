#Problemas Encontrados

* Utilização de proxy no OSX

Alguns comandos executados no terminal podem exigir o proxy, como por exemplo o homebrew (brew).
Isso pode ser contornado informando as configurações de proxy antes do comando, por exemplo,
para o comando:

	brew upgrade

utilizar:

	ALL_PROXY=http://<user>:<pass>@proxy.prodest.es.gov.br.local:8080 brew upgrade


###Referencias