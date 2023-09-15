<h1 align="center">
  File Storage API
</h1>

A sugestão é apresentada [nesse vídeo](https://youtu.be/b6kvS1Wszew?si=BAFcEpAqP6Pw4qMu) e mostra como implementar um file server utilizando Spring Boot.

## Tecnologias
 
- [Spring Boot](https://spring.io/projects/spring-boot)
- [Spring MVC](https://docs.spring.io/spring-framework/reference/web/webmvc.html)

## Como Executar

- Clonar repositório git:
```
git clone https://github.com/davidmateusreis/file-storage.git
```
- Construir o projeto:
```
./mvnw clean package
```
- Executar:
```
java -jar ./target/file-storage-0.0.1-SNAPSHOT.jar
```

## Testando Endpoints

- Upload file:
```
curl -X POST -F "file=@path/to/your/file.txt" http://localhost:8080/api/files/upload
```
- Download file:
```
curl -OJL http://localhost:8080/api/files/download/your-file-name.txt
```
- List uploaded files:
```
curl http://localhost:8080/api/files/list
```