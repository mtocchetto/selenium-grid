selenium-grid
=============

Arquivos e configurações de exemplo para usar o selenium grid

---
Hub
---

É o servidor do selenium grid.
Ele gerencia os nodos/browsers disponíveis e encaminha a execução dos testes para os nodos que estiverem livres. 

Para configurar o hub altere o arquivo hubconfig.json

----
Node
----

É onde ficam os browsers utilizados nos testes.
Cada node se registra a um hub e informa a ele os browsers existentes no nodo.

Para configurar o node altere o arquivo nodeconfig.json

**Atenção:** Caso necessário alterar no nodeconfig.json o valor da variável firefox_binary indicando o caminho do binário do firefox.

-------------------------------------
Como inicializar a estrutura do grid?
-------------------------------------

Iniciar o hub através do arquivo **hub.bat** ou utilizar o comando
```
  java -jar selenium-server-standalone-2.26.0.jar -role hub -hubConfig hubconfig.json
```

Iniciar o node através do arquivo **node.bat** ou utilizar o comando
```
  java -jar selenium-server-standalone-2.26.0.jar -role node -nodeConfig nodeconfig.json
```

Obs.: Este comando inicializa um nodo registrando-se ao selenium grid e informando a ele os browsers disponíveis


-----------
Referências
-----------

- https://code.google.com/p/selenium/wiki/Grid2
- https://code.google.com/p/selenium/wiki/DesiredCapabilities
- http://www.seleniumhq.org/docs/07_selenium_grid.jsp
