# Cadastro de Usuários
```http
  java -jar cadastro-usuario-0.0.1-SNAPSHOT.jar
```
- #### Abra a Database no seu navegador com o link:

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
