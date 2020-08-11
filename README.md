# Tabs CSS

  
![presentation](https://github.com/wandersonalwes/tabs-css/blob/master/.github/presentation.gif)

> Navegação através de guias, apenas com HTML e CSS.

  

Hey :wave:

  

Veja como é simples criar uma navegação em abas usando somente HTML e CSS.

Primeiro é necessário criar alguns inputs com `type="radio"`.

`<input id="login" type="radio" name="tabs" checked />`

`<input id="register" type="radio" name="tabs" />`

> Não esqueça de colocar o ID e deixar um dos inputs com o atributo checked.

Feito isso é necessário adicionar uma `label` pra cada input.


`<label class="tab" id="login" for="login">Entrar</label>`

`<label class="tab" id="register" for="register">Criar uma conta</label>`

> O atributo "for" de cada label deve corresponder ao atributo "id" do input.

Neste caso o atributo `class` e `id` será útil para manipulamos a visibilidade de cada guia, e personalizar o estilo.

Agora é só criar uma `div` com o conteúdo que você deseja mostrar em cada guia.

    <div class="panel" id="login">
      <p>Entrar</p>
    </div>

    <div class="panel" id="register">
      <p>Criar uma conta</p>
    </div>

**Seu código até o momento deve está assim:**

    <input id="login" type="radio" name="tabs" checked />
    
    <input id="register" type="radio" name="tabs" />
    
    <label class="tab" id="login" for="login">Entrar</label>
    
    <label class="tab" id="register" for="register">Criar uma conta</label>
    
    <div class="panel" id="login">
      <p>Entrar</p>
    </div>
    
    <div class="panel" id="register">
      <p>Criar uma conta</p>
    </div>

## Agora vem a mágica :smile:

    .panel {
      display: none;
    }
    
    #login:checked ~ .panel#login,
    #register:checked ~ .panel#register{
      display: block;
    }

Somente com esse trechinho de CSS a sua navegação já vai funcionar perfeitamente.  :wink:

O que a gente fez basicamente foi ocultar o conteúdo da nossa guia, e só mostrar-lo quando o nosso input estiver checado.

Pronto, é isso que acontece por debaixo dos panos neste exemplo. 
  



[![LinkedIn](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github)](https://github.com/wandersonalwes/) [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077b5?style=flat&logo=linkedin)](https://www.linkedin.com/in/wandersonalwes/)
