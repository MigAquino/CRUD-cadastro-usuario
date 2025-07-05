# Cadastro de Usuários
## Requisitos
- Java 21 ou maior
- para saber se tem o java instalado ou qual versão está instalada use o seguinte código no terminal:
```http
  java -version
```
- Caso tenha siga para a seção de Instalação
- Caso não tenha siga os passos abaixo:
- ### Windows:
  - Instale a versão LTS mais recente no link abaixo:
    
      [Java](https://www.java.com/pt-BR/) - Site oficial
  - Siga este tutorial para configurar o java:
    
      [Vídeo](https://www.youtube.com/watch?v=KwaGEF3asQQ) - Tutorial de configuração
- ### Linux:
  - Copie este comando no seu terminal:
```http
  sudo apt-get install default-jdk
```
## Instalação
- Baixa o arquivo .jar da release mais recente do projeto(v1.0.0) no link abaixo:

  [v1.0.0](https://github.com/MigAquino/CRUD-cadastro-usuario/releases/tag/v1.0.0) - Release mais recente

## Execução
- ### Windows:
  - Clique duas vezes no arquivo para executá-lo
  - Ou clique com o botão direito e abra com: OpenJDK Platform binary
- ### Linux:
  - No terminal vá para o diretório onde está localizado o arquivo utilizando o comando cd
  - Copie o comando abaixo: 
```http
  java -jar cadastro-usuario-0.0.1-SNAPSHOT.jar
```
- ### Após a execução abra a Database no seu navegador com o link:

```http
  http://localhost:8081/h2-console
```

#### Dados de acesso da database:
| Usuário   | Senha      | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `miguel` | `123` | **Obrigatório**. Login de acesso |

| JDCB URL   | Driver Class    | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `org.h2.Driver` | `jdbc:h2:mem:usuarios` | **Obrigatório**. Driver e URL da Database |


## Documentação da API
#### Dicas de uso
 - Recomendado utilizar o Postman para executar as funções abaixo

#### Cadastra um Usuário

```http
  POST localhost8081/usuario
```

| Body   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `email` | `string` | **Obrigatório**. Email do Usuario |
| `nome` | `string` | **Obrigatório**. Nome do Usuario |

#### Retorna um usuário por email

```http
  GET localhost8081/usuario?email=email_do_usuario
```

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `email`      | `string` | **Obrigatório**. O Email do usuário que quer buscar |

#### Atualiza o cadastro de um usuário

```http
  POST localhost8081/usuario?id=id_do_usuario
```
| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `id`      | `Integer` | **Obrigatório**. O id do usuário que quer atualizar |

| Body   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `email` | `string` | **Opcional**. Email do Usuario |
| `nome` | `string` | **Opcional**. Nome do Usuario |

#### Deleta um usuário

```http
  DELETE localhost:8081/usuario?email=email_do_usuario
```

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `email`      | `string` | **Obrigatório**. O Email do usuário que você quer deletar |
