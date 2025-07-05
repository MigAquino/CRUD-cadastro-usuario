
# Cadastro de Usuarios

Esse projeto foi desenvolvido para o meu aprendizado no desenvolvimento utilizando o Spring

## Rodando localmente
- #### Faca o download do arquivo .jar na ultima release

- #### Abra a Database no seu navegador com o link:

```http
  http://localhost:8081/h2-console
```

#### Dados de acesso da database:
| Usuario   | Senha      | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `miguel` | `123` | **Obrigatório**. Login de acesso |


## Documentação da API
#### Dicas de uso
 - Recomendado utilizar o Postman para executar as funcoes abaixo

#### Cadastra um Usuario

```http
  POST localhost8081/usuario
```

| Body   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `email` | `string` | **Obrigatório**. Email do Usuario |
| `nome` | `string` | **Obrigatório**. Nome do Usuario |

#### Retorna um usuario por email

```http
  GET localhost8081/usuario?email=email_do_usuario
```

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `email`      | `string` | **Obrigatório**. O Email do usuario que quer buscar |

#### Atualiza o cadastro de um usuario

```http
  POST localhost8081/usuario?id=id_do_usuario
```
| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `id`      | `Integer` | **Obrigatório**. O id do usuario que quer atualizar |

| Body   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `email` | `string` | **Opcional**. Email do Usuario |
| `nome` | `string` | **Opcional**. Nome do Usuario |

#### Deleta um usuario

```http
  DELETE localhost:8081/usuario?email=email_do_usuario
```

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `email`      | `string` | **Obrigatório**. O Email do usuario que você quer deletar |
