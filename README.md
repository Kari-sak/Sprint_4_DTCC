# SouLutions
- Para rodar o programa, precisa-se abrir o projeto como Maven. Para rodá-lo, deve-se procurar o arquivo nomeado como "DbeSoulCoderzApplication.java", clicar com o botão direito, selecionar a opção "Run as", e logo em seguida, selecionar a opção "Java Application".

- Para visualizar o projeto funcionando, deve-se abrir o navegador para ver os endpoints. A url base que deve ser acessada deve ser "http://localhost:8080". Depois disso, deve-se adicionar os seguintes paths adicionais:

### Lista de endpoints 

-`/planos`
> METHOD: GET
> 
> HEADER:
> Content-Type: application/json
> Authorization: Bearer {chave de identificação do usuário da SouLutions}
> 
>---
>
>200 OK - caso aparecam os usuários;
>204 No Content - caso não existam usuários cadastrados;
>401 Unauthorized - caso não esteja logado;
>500 Internal Server Error - caso dê qualquer erro inesperado.
>
>---
>
>Descrição:
>Devolve todos os planos cadastrados


-`/suporte`
> METHOD: GET
> 
> HEADER:
> Content-Type: application/json
> Authorization: Bearer {chave de identificação do usuário da SouLutions}
> 
>---
>
>200 OK - caso aparecam os usuários;
>204 No Content - caso não existam usuários cadastrados;
>401 Unauthorized - caso não esteja logado;
>500 Internal Server Error - caso dê qualquer erro inesperado.
>
>---
>
>Descrição:
>Devolve todos as solicitações de suporte cadastrados

-`/feedback`
> METHOD: GET
> 
> HEADER:
> Content-Type: application/json
> Authorization: Bearer {chave de identificação do usuário da SouLutions}
> 
>---
>
>200 OK - caso aparecam os usuários;
>204 No Content - caso não existam usuários cadastrados;
>401 Unauthorized - caso não esteja logado;
>500 Internal Server Error - caso dê qualquer erro inesperado.
>
>---
>
>Descrição:
>Devolve todos os feedback cadastrados

-`/feedback/formulario`
> METHOD: GET
> 
> HEADER:
> Content-Type: application/json
> Authorization: Bearer {chave de identificação do usuário da SouLutions}
> 
>---
>
>200 OK - caso aparecam os usuários;
>204 No Content - caso não existam usuários cadastrados;
>401 Unauthorized - caso não esteja logado;
>500 Internal Server Error - caso dê qualquer erro inesperado.
>
>---
>
>Descrição:
>Mostra o arquivo HTML referente ao formulário do feedback.


-`/feedback/novo`;
-`essa solicitação é uma endpoint a ser lida pelo backend apenas, e não retorna nenhum visual. Para ver a sessão de cadastro, deve-se digitar a url "localhost:8080/feedback/formulario"`
> METHOD: POST
> 
> HEADER:
> Content-Type: application/json
> Authorization: Bearer {chave de identificação do usuário da SouLutions}
>
> BODY:
> {
> &nbsp; &nbsp;  "messages": [
> &nbsp; &nbsp; &nbsp; &nbsp;    { "role": {emissor da mensagem}, "content": {conteúdo} },
> &nbsp; &nbsp; &nbsp; &nbsp;    { "role": {emissor da mensagem}, "content": {conteúdo} },
> &nbsp; &nbsp; &nbsp; &nbsp;    { "role": {emissor da mensagem}, "content": {conteúdo} },
> &nbsp; &nbsp; &nbsp; &nbsp;    ...
> &nbsp; &nbsp;  ]
> }
>
>---
>
>200 OK - caso a mensagem tenha sido enviada e respondida;
>400 Bad Request - caso dê algum erro na emissão do cabeçalho ou do corpo da requisição;
>401 Unauthorized - caso não esteja logado;
>500 Internal Server Error - caso dê qualquer erro inesperado e quando a OpenAI API responder com um código 500.
>
>---
>
>Descrição:
>Cadastra novo feedback no banco de dados.


-`/usuario/{id}`
> METHOD: GET
> 
> HEADER:
> Content-Type: application/json
>Authorization: Bearer {chave de identificação do usuário da SouLutions
>
>---
>
>200 OK - caso apareca o usuário escolhido;
>204 No Content - caso não existam usuários cadastrados;
>401 Unauthorized - caso não esteja logado;
>500 Internal Server Error - caso dê qualquer erro inesperado.
>
>---
>
>Descrição:
>Devolve o usuário cujo id é recebido do path

`/usuario/formulario`
> METHOD: GET
> 
> HEADER:
> Content-Type: application/json
> Authorization: Bearer {chave de identificação do usuário da SouLutions}
> 
>---
>
>200 OK - caso aparecam os usuários;
>204 No Content - caso não existam usuários cadastrados;
>401 Unauthorized - caso não esteja logado;
>500 Internal Server Error - caso dê qualquer erro inesperado.
>
>---
>
>Descrição:
>Mostra o arquivo HTML referente ao formulário do usuario.

-`/usuario/novo`;
-`essa solicitação é uma endpoint a ser lida pelo backend apenas, e não retorna nenhum visual. Para ver a sessão de cadastro, deve-se digitar a url "localhost:8080/usuario/formulario"`
> METHOD: POST
> 
> HEADER:
> Content-Type: application/json
> Authorization: Bearer {chave de identificação do usuário da SouLutions}
>
> BODY:
> {
> &nbsp; &nbsp;  "messages": [
> &nbsp; &nbsp; &nbsp; &nbsp;    { "role": {emissor da mensagem}, "content": {conteúdo} },
> &nbsp; &nbsp; &nbsp; &nbsp;    { "role": {emissor da mensagem}, "content": {conteúdo} },
> &nbsp; &nbsp; &nbsp; &nbsp;    { "role": {emissor da mensagem}, "content": {conteúdo} },
> &nbsp; &nbsp; &nbsp; &nbsp;    ...
> &nbsp; &nbsp;  ]
> }
>
>---
>
>200 OK - caso a mensagem tenha sido enviada e respondida;
>400 Bad Request - caso dê algum erro na emissão do cabeçalho ou do corpo da requisição;
>401 Unauthorized - caso não esteja logado;
>500 Internal Server Error - caso dê qualquer erro inesperado e quando a OpenAI API responder com um código 500.
>
>---
>
>Descrição:
>Cadastra novo usuário no banco de dados.
