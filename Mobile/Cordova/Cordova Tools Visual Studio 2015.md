# Instalação

A instalação é integrada com o Visual Studio 2015

Devido ao nosso proxy corporativo é recomendado que não se instale nenhuma ferramenta
de terceiros pelo instalador do VS, porque todos esses componentes sao baixados na hora
da instalação e ela não reconhece o proxy. A instalação deve ser feita manualmente depois.

# Configuração de Componentes de Terceiros

## ​​​Pré-requisitos​

​Java e Ant instalados e configurados no PATH

* ​​Instalar NodeJs versão 0.10.33 x86

​​​​​​​​​A versão 0.12.2 apresenta um erro ao instalar as plataformas, mesmo com o proxy configurado (O erro acontece devido ao proxy. É um problema no NodeJs)

Adicionar ao PATH nas variávels de ambiente:

PATH += C:\Program Files (x86)\nodejs​ (de acordo com a instalação)

PATH += C:\Users\<usuario>\AppData\Roaming\npm (de acordo com a instalação)​

* Instalar os SDKs que serão utilizados (android, iOS, WP etc.)

Para o android, adicionar ao PATH:

PATH += C:\Program Files (x86)\Android\android-sdk\tools​ (de acordo com a instalação do android SDK)

*Obs Android: Caso necessário atualizar pacotes com o SDK Manager configurar o proxy pelo IP, atualmente 10.0.0.18​, porta 8080. Sempre executar como administrador*

* ​Configurar o proxy no npm

​​​O npm é instalado junto com o NodeJs, mas não funcinoa direito devido ao proxy do Prodest. 
Por isso os comandos abaixo devem ser executados:

	​npm config set proxy http://<usuario>:<senha>@proxy.prodest.es.gov.br.local:8080/
	npm config set https-proxy http://<usuario>:<senha>@proxy.prodest.es.gov.br.local:8080/
	npm config set registry http://registry.npmjs.org/

Pode ser utilizado o comando `npm config edit` para edição de todas as configurações

* Instalar Cordova 4.3.0

	npm install cordova@4.3.0 -g​

### Observações

Verificar necessidade de instalar o Git Client​

1. Todos os comandos devem ser executados em um prompt de comando no modo administrador
2. "-g" diz ao npm para instalar o pacote globalmente


Após esses passos já será possivel criar aplicações e compilar

### Referências

Documentação sobre o cordova feita pela Microsoft: https://github.com/Microsoft/cordova-docs​

Configuração geral: https://msdn.microsoft.com/pt-br/library/Dn771551.aspx

NodeJs 0.10.38 para windows: http://nodejs.org/dist/v0.10.38/node-v0.10.38-x86.msi​

Android SDK: http://developer.android.com/sdk/index.html​

Npm udpate: https://docs.npmjs.com/getting-started/installing-node