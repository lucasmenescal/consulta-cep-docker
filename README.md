**Infra-Docker da API REST de Consulta Endereço via CEP**

### Como rodar o projeto usando Docker
1. **Faça o git clone deste projeto em uma pasta de sua preferencia.**
2. Clone o repositorio da API REST dentro da pasta /calcula-frete-infra/projeto
  `git clone https://github.com/lucasmenescal/consulta-endereco.git`

3. Abra um terminal de comando dentro da pasta **consulta-cep-infra** e digite
`docker-compose up -d`
4. Aguarde finalizar e aguarde o mvn rodar as instalações necessárias e iniciar a API.


[Link da API](https://github.com/lucasmenescal/consulta-endereco)


### Requisitos
1. Ter o docker e o docker-compose instalados na maquina.
2. Ter o vscode instalado
3. Ter a extensao Dev container instalado no vscode

### Observações importantes
1. Para conseguir rodar os testes Junit5, Cucumber é necessário comentar a linha `command: mvn spring-boot:run` do docker-compose e descomentar `command: /bin/bash`
2. Em seguida, deverá abrir um vscode dentro do container, com a extensao Dev containers.
3. Abrir um terminal dentro do container e digitar `mvn test`

### Para acessar a Documentação Swagger
1. Quando a API estiver rodando dentro do container acesse o link:
[Documentação Swagger](http://localhost:8080/swagger-ui/index.html)
