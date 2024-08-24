# Integração de Leitor Biométrico (Beta Version)
Passos para instalar e utilzar um leitor biométrico para transferir texto FIR à um navegador de internet

## 1. Instalação do Driver

Segue o link do fabricante para os drivers mais recentes do leitor biométrico modelo `Hamster III` da Fingertech e acesso aos respectivos manuais de instalação.

- [Listagem de drivers por sistema operacional e manuais de instalação](http://suporte.fingertech.com.br/leitores-biometricos/) 

## 2. Instalação do JDK

**OBS:** essa etapa é opcional caso já tenha uma JDK instalada.

Segue os links para instalação do JDK da Oracle.

- [Download JDK Windows](https://www.oracle.com/java/technologies/downloads/#jdk22-windows)
- [Download JDK Linux](https://www.oracle.com/java/technologies/downloads/#jdk22-linux) 

## 3. Instalação do SDK

Segue os link do fabricante para download do SDK Nitgen da Fingertech.

- [Listagem de SDKs por sistema operacional e códigos de exemplo por linguagem de programação](http://suporte.fingertech.com.br/devs-download-sdk/)

## 4. Execução de arquivo JAR

Faça o download do arquivo `restAPIhamsterIII.zip` e descompacte em um diretório de sua preferência.

Por meio de `CLI`, vá até o diretório do arquivo `JAR` descompactado e digite o comando:

``` bash
java -jar HamsterIIIRESTAPI-0.0.1-SNAPSHOT.jar
```

Um servidor web autocontido será iniciado e responderá apenas requisições `GET` por meio da URI `localhost:1989/fingerprint`, devolvendo uma resposta em formato `JSON` contendo três campos:

- `ID`: identificador do dedo em que foi verificada a impressão digital;
- `name`: descrição de qual dedo foi verificada a impressão digital;
- `fingerprint`: os dados em formato de texto da impressão digital recolhida.
