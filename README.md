# Mao-na-massa-aula-7-Javascript-PT2

Vamos agora adicionar uma pequena animação na remoçao de cada paciente, fazendo uma mistura de técnicas de CSS e Javascript.

1- Vamos adicionar um CSS que será responsável por animar a remoção. Em seu index.css faça:

    //index.css

    .fadeOut {
        opacity: 0;
        transition: 0.5s;
    }

Essa classe que deveremos adicionar ao elementos que vamos remover.

2- Vamos utilizar a técnica vista no vídeo, de aplicar a classe, chamar a função setTimeout para aguardar a animação terminar e ao fim dela, remover o elemento dá página. Primeiro adicione a classe na <tr>:

    var tabela = document.querySelector("#tabela-pacientes");

    tabela.addEventListener("dblclick", function(event) {
        event.target.parentNode.classList.add("fadeOut");

        event.target.parentNode.remove();


    });

3- Agora vamos utilizar a setTimeout para aguardar antes de remover:

    var tabela = document.querySelector("#tabela-pacientes");

    tabela.addEventListener("dblclick", function(event) {
        event.target.parentNode.classList.add("fadeOut");

        setTimeout(function() {
            event.target.parentNode.remove();
        }, 500);

    });

Deste modo, quando o usuário clicar para remover um paciente, ele vai esmaecer por meio segundo antes de sumir!
