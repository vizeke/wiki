# Criando Pacote

* ​​Criar cha​ve p​ara assinar aplicativo

keytool -genkey -keyalg RSA -alias alias_name -keystore mykeystorename.keystore -storepass mykeystorepass -validity 10000 -keysize 2048​
 Serão solicitadas algumas informações na criação, auto explicativo.

* Configurar chave no app cordova

Local do arquivo no projeto: /res/native/android/ant.properties

	key.store=mykeystorename.keystore
	key.alias=alias_name 
	key.store.password=<senha>
	key.alias.password=<senha>

* Compilar Projeto

* Copiar APK para Google Play

TODO: Melhorar explicação dessa pagina

# Publicação