FROM ubuntu
# Instala o OpenJDK 17
RUN apt update && apt install -y openjdk-17-jdk
# Define o diretório de trabalho
WORKDIR /opt/educare-file-commons/
# Copia o arquivo JAR para o contêiner
COPY file-commons.jar /opt/educare-file-commons/filecommons.jar
# Define uma variável de ambiente para o perfil Spring
ENV SPRING_PROFILE=default
# Comando para executar a aplicação com o perfil Spring especificado
CMD ["sh", "-c", "java -jar -Dspring.profiles.active=$SPRING_PROFILE filecommons.jar"]
# Expõe a porta
EXPOSE 8444
