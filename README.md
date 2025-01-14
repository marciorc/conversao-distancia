# conversao-distancia

## comandos importantes
- `docker build -t conversao-distancia -f Dockerfile .`  
Cria a imagem a partir da receita descrita no Dockerfile  

- `docker container run -d -p 8181:5000 conversao-distancia`  
Executa o container passando os seguintes parametros  
-d = daemon  
-p = port  