+++
title = "Gerenciando versões JDK de forma mais simples"
tags = ["jdk", "java", "linux"]
+++ 
Pra facilitar a troca de versão do JDK (Java Development Kit) diversas vezes na mesma máquina, descobri recentemente uma ferramenta que ajudou nisso: o [SDKMan](https://sdkman.io/ "Página Inicial do SDKMan"). No Linux (e no Windows via WSL2), a instalação é coisa simples: 

{{<cmd>}}
curl -s "https://get.sdkman.io" | bash && source "$HOME/.sdkman/bin/sdkman-init.sh"
{{</cmd>}}


Você consegue conferir a instalação com um: {{<cmd>}}sdk version{{</cmd>}}

Para efetivamente instalar as versões JDK desejadas, é possível escolher entre diferentes builds e versões disponíveis na listagem exibida ao executar: 
{{<cmd>}}sdk list java{{</cmd>}}

Com base no Identifier da versão, já é possível instalar a versão desejada com o SDKMan com o comando `sdk install java identificador`, ex: {{<cmd>}}sdk install java 21.ea.35-open{{</cmd>}}

Caso tenha sido instalada mais de uma versão, é possível definir a versão padrão do sistema operacional com: {{<cmd>}}sdk use java 21.ea.35-open{{</cmd>}}

Além disso, o SDKMan pode ajudar na instalação de outras ferramentas bastante utilizadas, como: Tomcat, Maven, dentre outras listadas em [SDK Installation Candidates](https://sdkman.io/sdks "Página de SDKs disponíveis para instalação").

A instalação pode ser feita com sintaxe semelhante à instalação do JDK, ex: {{<cmd>}}sdk install maven{{</cmd>}}