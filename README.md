# Criação do projeto:

* ng new "nome do projeto"

**primeira pergunta: Angular routing - dar um Yes** 

- selecionar o CSS mesmo nos estilos

abrir a pasta do projeto no VSCode, abrir o arquivo `"package.json"` e ficar de olho nas `dependencies`.

rodar os comandos de instalação das dependencias:
```npm install bootstrap
npm install jquery
npm install popper.js
npm install ngx-bootstrap
npm install ngx-order-pipe
```
trocar a versão do bootstrap: trocar o numero da versão no package.json para `4.5.3`, e rodar um **npm install** no terminal

colocar os caminhos do bootstrap/jquery/popper dentro do angular.json
```"styles": [
              "src/styles.css",
              "./node_modules/bootstrap/dist/css/bootstrap.min.css"
            ],
            "scripts": [
              "./node_modules/jquery/dist/jquery.js",
              "./node_modules/popper.js/dist/umd/popper.min.js",
              "./node_modules/bootstrap/dist/js/bootstrap.js"
            ]
``` 
pra testar, vai no app.component.html, apaga tudo que tem, e colocar um 
`<h1 class="text-danger ml-5">testando</h1>`
se ficar com o texto vermelho, e um pouco pra direita da tela, ta tudo certo.

* comando para criar novos componentes:
```
ng generate component "nome do componente"
ou
ng g c "nome do componente"
 ```

>**Dicas de formulário...**
sempre criar os labels e inputs dentro de uma TAG form, pra funcionar o "enter" no botão de login, por exemplo

<hr>

### Criação das Services e Models

> A criação das models será feita de forma manual, criando dentro da pasta APP, uma pasta de model, e criando os arquivos para cada uma das models do Backend, com a extensão .ts
> `Usuario.ts` por exemplo.

Ao criar as models, sempre criar com o padrão:
``` 
export class "Nome da model" {
	public "atributo": "tipo"
}
```
Na hora de configurar a service, será necessário adicionar o HttpClientModule dentro do `app.module.ts`, conforme a documentação do Angular:

[Documentação oficial do HTTP no Angular](https://angular.io/guide/http)

