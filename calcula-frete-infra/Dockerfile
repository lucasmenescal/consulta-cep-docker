# Define a imagem base que será utilizada
FROM maven:3.8.4-openjdk-11-slim

# Instalações necessárias
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install unzip -y
RUN apt-get install locales -y
RUN apt-get install wget -y

# Configurações de Container
RUN echo "America/Recife" > /etc/timezone
RUN apt-get install -y locales locales-all
RUN sed -i -e 's/# pt_BR.UTF-8 UTF-8/pt_BR.UTF-8 UTF-8/' /etc/locale.gen && \locale-gen
RUN dpkg-reconfigure -f noninteractive tzdata

# Instalando spring-CLI
WORKDIR /spring-cli
RUN wget https://repo.spring.io/release/org/springframework/boot/spring-boot-cli/2.6.3/spring-boot-cli-2.6.3-bin.zip
RUN unzip spring-boot-cli-2.6.3-bin.zip -d spring-boot-cli
RUN export PATH=$PATH:/spring-cli/spring-boot-cli/spring-2.6.3/bin

# Define o diretório de trabalho
WORKDIR /workspace

# Para Criar a API REST(Projeto inicial)
RUN spring init --dependencies=web,actuator --language=java --boot-version=2.5.0 --java-version=11 consulta-endereco --build mvn
RUN cd consulta-endereco
RUN mvn compile






