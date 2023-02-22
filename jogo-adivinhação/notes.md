Projeto jogo da advinhação //foco total//


                                INICIANDO HTML E CSS

PASSO UM: criei os arquivos index.html, style.css e script.js abri o figma para ter melhor visualização.

PASSO DOIS: inseri o layout e estrutura do html tudo normal e botei o link do css.

PASSO TRES: copiei o background do body do figma, e colei no meu body do css.

PASSO QUATRO: criei uma tag main para fazer a caixa que tem o botão, analisei passo a passo o que fazer pelo figma, começando com tamanho e largura da caixa, tags (h1, p e button), e cores e fonts.

PASSO CINCO: botei o css background, box-shadow, border-radius (figma).

PASSO SEIS: ajustei o :root, 
        font-size:62.5%;  (para ficar mais responsivo)

        e no body
         font-size:1.6rem;  (para todos os itens ficarem c 1.6rem)

         e substitui todos os pixels por rem

PASSO SETE: Ajustei tambem o padding 4.8rem(top) 6.4rem(laterais), 6.4rem(down) e ja resetei o margin e padding com um seletor universal *{
    padding:0;
    margin:0;
    box-sizing:border-box;
}

PASSO OITO: Logo depois coloquei o width no main
width: min(42.8rem, 90%)
o minimo da pag e 42.8 e se a tela diminuir vai ficar 90% nas laterais praticamente a mesma coisa.

PASSO NOVE: coloquei um display grid no body, pois o body só tem um filho que seria o main

body{
    background:...;
    font-size:...;
    
    display:grid;
    place-items: center;(vai centralizar o filho do body no meio da pag)
    height:100vh;
}

PASSO DEZ: botei um margin-top -12rem para fazer um pequeno ajuste  no meu main


                                    FONTES E TEXTOS 


PASSO ONZE: Comecei botando um H1 no section, e uma tag P abaixo, criei um form com o input e button.

PASSO DOZE: Abri o google fonts e fui atras das fontes que tinha para colocar no projeto

PASSO TREZE: E fui colocando as fontes em suas respectivas tags

PASSO QUATORZE: Coloquei um text-align:center; para alinhar todos os textos

PASSO QUINZE: Logo após eu começei a ajusta o tamanho das fontes, e já ajustei a separação entre elas

PASSO DEZESSEIS: Botei as cores dos textos como h1 e p

PASSO DEZESSETE: O P tinha uma opacity de .8rem para ficar mais transparente


                                    INPUT E BUTTON  

PASSO DEZOITO: Resetei o button e o input, tirando a borda e botando um padding.

PASSO DEZENOVE: Coloquei o background no input e no button.

PASSO VINTE: Existia uma separação entre o input e button entao no form eu coloquei um display flex para deixar eles grudados

PASSO VINTE E UM: Ajustei o tamanho do input e button e já alinhei eles com um justify-content center no FORM

PASSO VINTE E DOIS: botei o border radius no button, como tinha um border radius no button e no input e eles estão um do lado do outro eu tive que fazer o border radius assim:

            border-radius: 0 .4rem .4rem, 0

            //E no input

            border-radius: .4rem 0 0 .4rem


                                    FINALIZANDO TELAS 

PASSO VINTE E TRES: Para criar duas telas eu criei uma div "Screen1" que pega todo código até o form e botei uma classe hide

<div class "Screen1 hide">
    ...
</div>

PASSO VINTE E QUATRO: separei no style o que era screen 1 no style.css é preciso falar que hide é display none

.hide{
    display:none
}

PASSO VINTE E CINCO: Depois criei uma div Screen 2 abaixo da div do screen 1

PASSO VINTE E CINCO: A lógica por trás disso é para ter a divisão de telas quando eu botar o JS
pois ai quando eu clicar no botão ele vai fazer  com que troque as telas, uma recebe hide e outra fica aberta.

PASSO VINTE E SEIS: Criei o quê tinha na tela 2 que era um h2 e um botão e agora vou formatar eles (font-size, font-family, cores etc).

PASSO VINTE E SETE: Ajustei a divisão de um para outro e as bordas.

PASSO VINTE E OITO: Botei as classes gerais como main, body, button, hide em cima todas agrupadas para não ter erro e melhor visualização.

PASSO VINTE E NOVE: Botei um button:hover com um azul mais forte no botão para dar um destaque.

PASSO TRINTA: Botei tambem um transition no botão 

    transition:background(onde aplicar) .3s

                                    INTRODUÇÃO A DOM

/*
    Explicação do conteúdo

    O quê é DOM: Document Object Model: Modelagem do documento como javascript.

    Representação do HTML em Objetos JavaScript: atributos(propriedades ex celular: cor, peso...) e métodos(funcionalidades ex celular: ligar, falar pela internet...)

    criada pelo navegador(browser):  É uma interface(API) usada no navegador.

    A DOM é a ponte entre HTML e JS para manipular elementos HTML, estilos e até disparar ação

    (A DOM não é javascript, é apenas a representação do HTML em formato de um objeto JS)

    O document de uma página seria tudo na pag, se eu abrir o DevTools e no console escrever "document" e dar enter 
    vai simplesmente mostrar que é toda página\


*/

                                     Manipulando a DOM

/*
    As tags HTML, quando usadas pela DOM, podemos chamar de node (nó) ou de element (elemento)

    //pegando um elemento
    
    const h1 = document.querySelector('h1') //HTMLElements

    declaro uma variavel e puxo o H1 do meu HTML para o JS e vou me referenciar a ele pelo nome da variavel

    //Pegando varios elementos

    const links = document.querySelectorAll('a') //NodeList

    //Podemos pegar qualquer valor das tags e, tambem alterar eles.

    //InnerText
    console.log(h1.innerText)
    ("o que tem no h1")

    links[30].innerText
    'nivel 4'  é o que tem nesse link

    //Dá para alterar o texto (ou o HTML)

    h1.innerText = "Novo título" (dentro das aspas ta o valor atribuido)

    //Dá para atribuir estilos tambem

    h1.style.backgroundColor = "green"

    //Adicionando classes 

    const h1 = document.querySelector("h1")

    h1.classList.add('hide')
    (poem uma classe hide que vai fazer ele ficar invisivel)
    
    //Removendo classes

    onst h1 = document.querySelector("h1")

    h1.classList.remove('hide')

    (remove a classe hide)

    //alterando entre classes

    onst h1 = document.querySelector("h1")

    h1.classList.toggle("hide")
    (Se não tiver a classe adiciona e se não tiver na hora que rodar denovo tira a classe)
*/

                                    CAPTURANDO VALOR DO FORMULARIO AO CLICAR NO BOTÃO


PASSO TRINTA E UM:Comecei botando a tag script no meu html botei antes de fechar o body.

PASSO TRINTA E DOIS:O objetivo aqui é pegar o valor do form, e fazer com que a pagina não fique atualizando

PASSO TRINTA E TRES: //script
                    No main.js comecei criando uma função chamada de 
                    handleClick(){

                    }

                    //HTML

                    no button eu coloquei uma função que se chama onclick = ""
                    nela eu botei a minha function handle click

                    <button onclick = "handleClick()">Tentar</button>

                    ou seja ao clicar nesse botão vai executa o meu JS

                    //MAIN.JS

                    coloquei um console log na função do handle click para ver se funcionava certinho
                    então toda vez que eu clicava no botão da pagina aparecia a mensagem que eu coloquei no console.log, porem ela não permanecia justamente por causa do button estar dentro de un formulario ele reseta a pagina sempre depois do click.

                    para isso não acontecer eu coloquei um parametro chamado event na minha função, e um event.preventDefault().

                    function handleClick(event) {
                        event.preventDefault()
                        console.log("cheguei aqui")
                    }

                    //HTML

                    <button onclick = "handleClick(event)">Tentar</button>

                    Com isso quando eu clicar no botão a página não sera recarregada]

                    botei um ID no input para poder chamar ele com a DOM 

                    //Main.js

                    dentro da function eu chamei o input com a DOM

                     function handleClick(event) {
                        event.preventDefault()

                        const inputNumber = document.querySelector("#inputNumber")
                        console.log(inputNumber.value)
                    }

                            (.value para mostrar o valor)

                    agora o console vai imprimir o valor que tiver no input
                                         

                                APLICANDO A LÓGICA

PASSO TRINTA E QUATRO: Primeira coisa foi pegar uma parte do projeto 04 do stage 04 que era a mesma coisa porem com JS ao inves de JS CSS E HTML

                        const randomNumber = Math.round(Math.random() *10)
                        Math.round() arredonda o valor de um numero para o inteiro mais próximo

                        Math.random() 
                        Vai pegar um número aleatório entra 0 e 1
                        
                        agora
                    
                        Math.random() * 10
                        vai pegar um número aleatório entre 0 e 10

                         const randomNumber = Math.round(Math.random() *10)
                            Tá criando uma variavel e recebendo um Math.round e dentro desse Math.round tem um
                            Math.random que vai de 0 a 10 por causa do Math.round


PASSO TRINTA E CINCO: Coloquei uma variavel com número de tentativas

                        O código até agora fica assim:

                        const randomNumber = Math.round(Math.random() *10)
                        //para dar o numero aleatorio
    
                        let xAttmpts = 1
                        //numero de tentativas

                        function handleClick(event) {
                        event.preventDefault()

                        const inputNumber = document.querySelector("#inputNumber")
                        console.log(inputNumber.value)
                        //chamei o Input com a DOM, e botei no console.log(inputNumber.value) para saber o valor do inputNumber e para saber o valor tem que ter o .value
                        }
                        // function para rodar as coisas

PASSO TRINTA E SEIS: botei a variavel do numero de tentativas dentro da function com um ++
                        xAttempts ++
                        para ela sempre somar quando acontecer alguma coisa
                        
                        e já tirei o console.log, com essa variavel de controle dentro da minha function ela vai somar cada tentativa depois q eu clicar


                         const randomNumber = Math.round(Math.random() *10)
                        //para dar o numero aleatorio
    
                        let xAttmpts = 1
                        //numero de tentativas

                        function handleTryClick(event) {
                        event.preventDefault()

                        const inputNumber = document.querySelector("#inputNumber")

                        xAttempts ++
                        }
                        // function para rodar as coisas

                        o xAttempts ++ tem que ficar no final da aplicação sempre para quando acontecer tudo ele somar

PASSO TRINTA E SETE: para poder ver se a pessoa errou ou quando acertasse eu criei um IF, com esse if eu fiz com que o input seja number e se ele fosse == igual ao randomNumber ele adicionaria a classe hide no screen1

                    if(Number(inputNumber.value) == randomNumber){
                        document.querySelector(".screen1").classList.add("hide")
                        document.querySelector(".screen2").classList.remove("hide")
                    }

                    eu já mexi direto na DOM então não precisar chamar uma variavel eu já chamei direto no próprio if, não da para chamar o inputNumber sem o .value se fizer isso ele não vai ter nenhum numero

                    O que ta acontecendo ali 

                    se(if) inputNumber.value for igual a random number a DOM vai puxar a classe screen1 e vai adicionar um hide pra ela e remover o da screen2

                    mas se não for igual ele não vai fazer nada apenas contabilizar os erros

PASSO TRINTA E OITO: o próximo passo e mudar o innerText do h2 e isso é muito facil

                

                    if(Number(inputNumber.value) == randomNumber){
                        document.querySelector(".screen1").classList.add("hide")
                        document.querySelector(".screen2").classList.remove("hide")

                        document.querySelector(".screen2 h2").innerText = `você acertou em ${xAttempts} vezes`
                    }

                    é a mesma coisa dos outros eu não preciso puxar uma variavel apenas colocar direto na DOM, da para chamar mais de uma classe no mesmo document
                    

                                        EVENTOS


                    Explicação sobre eventos:
                        
                        Event-driven: A DOM é direcionada a eventos "Event-driven". significa que ela podera reagir
                        a qualquer tipo de evento relacionado à página.

                    Podemos entender em 2 fases:
                        A ocorrência do evento e a reação à essa ocorrência

                    Eventos:
                        Ações que acontecem na página, site ou aplicação.

                        *Carregamento do documento, aparição de elementos na tela.
                        *Modificação de propriedades da página (largura, altura, scroll).
                        *cliques de mouse e digitação do teclado.
                        *interação com sons, imagens, vídeos.
                        *outros

                    Reações 
                        O sistema poderá executar reações às ações. Executando uma função sempre que
                        determinada ação acontecer.


                    EXEMPLO
                        Ao clicar em um botão, apresenta em tela um elemento que estava escondido.


                                HTML
                        
                        <button>clique</button>

                        <p class = "hide">escondido </p>


                                CSS

                        .hide{
                            display:none
                        }


                                JS

                        const button = document.querySelector("button")

                        //vamos registrar o evento na mesma aplicação
                        button.addEventListener('click', function(e){
                            console.log(e) //objeto contendo tudo sobre o evento

                            document.querySelector('p').style.display = "block"
                        })                     

                        ao clicar no botão vai acionar o evento 'click' e quando acionado vai rodar a função callback e com isso vai adicionar um display block no <p> q tava como none,
   
                        //addEventListener recebe 2 argumentos
                        // O primeiro é uma string com nome do evento ou seja 'click' todas vez que clicar no botão 
                        vai fazer rodar a função callback
                        // depois, uma função callback
                        // que irá executar um código em reação ao evento


                        Outra maneira de fazer

                         const button = document.querySelector("button")

                        button.addEventListener('click', buttonClick)


                         function buttonClick(e){
                            document.querySelector('p').style.display = "block"
                         }       

                         a função callBack tem que ser chamada (buttonClick)

                         (eu acho melhor assim mais organizado)


                                        APLICANDO EVENTOS E CALLBACKS


PASSO TRINTA E NOVE: Tirei a onclick do button, pois n e a função do HTML fazer o que o js tem que fazer,
após tirar eu coloquei um ID nos dois buttons para puxar com a DOM

PASSO QUARENTA: Chamei os botões para o JS com a dom (documente.querySelector(''))

PASSO QUARENTA E UM: Registrei os eventos:

                        btnTry.addEventListener('click' handleTryClick)
                            (troquei o nome da função handleClick para handleTryClick para ficar mais semantico quando eu fosse me referir a esse evento)                      


                        btnTry.addEventListener('click' handleTryClick)

                        handleTryClick só vai rodar quando ele receber um click pois handleTryClick é argumento da função eventListener e sem esse 'click' ela não roda                        


PASSO QUARENTA E DOIS: Botei o screen2 e o screen1 em variaveis para ficar mais simples de chama-los

PASSO QUARENTA E TRES: Registrei o evento do btnReset com uma função anonima

                        btnReset.addEventListener('click' function(){
                            //ao clicar vai remover o hide do screen1 e add no screen2
                            screen1.classList.remove("hide")
                            screen2.classList.add("hide")

                            xAttempts = 1
                            //e vai reseta o numero de tentativas
                        })

                        e com isso está praticamente pronto
                            

                                REFATORANDO O CÓDIGO



PASSO QUARENTA E QUATRO: Botei todas as variaveis juntas em um só lugar na parte superior do código

PASSO QUARENTA E CINCO: Troquei o jeito q eu fiz o evento do resetClick chamei uma função callBack ao inves de anonima

            function handleResetClick(){
                screen1.classList.remove("hide")
                 screen2.classList.add("hide")

                  xAttempts = 1
            }

            btnReset.addEventListener('click', handleResetClick)

PASSO QUARENTA E SEIS: Melhorei a lógica, criei uma função para o screen1 e o screen2 do botão de tentar novamente
essa função ta sendo chamada dentro da função handleResetClick(){} e da função handleTryClick dentro if


            function handleTryClick(event){
                event.preventDefault()

                const inputNumber = document.querySelector("#inputNumber")

                    if(Number(inputNumber.value) == randomNumber){
                       toggleScreen()

                        document.querySelector(".screen2 h2").innerText = `você acertou em ${xAttempts} vezes`
                    }
                    
                    inputNumber.value = ""
                    xAttempts++

                    }

             function handleResetClick(){
               toggleScreen()

                xAttempts = 1
            }


            function toggleScreen(){
                screen1.classList.toggle('hide')
                screen2.classlist.toggle('hide')
            }

            dessa maneira fica mais simplificado 

PASSO QUARENTA E SETE: Fiz um evento para rodar mesmo se eu clicar com enter nele

    document.addEventListener("keydown", function(e){
        if(e.key == 'Enter' && screen1.classList.contains('hide')){
            handleResetClick()
        }
    })
    
    se a tecla do evento for enter rodar handleResetClick() so vai rodar se screen1 tiver a classe 'hide'

PASSO QUARENTA E OITO: Botei o randomNumber no handleResetClick para toda vez q eu der enviar novamente ele trocar de numero 



                                            PROJETO BISCOITO DA SORTE


                        Animações:
                        @keyFrames topdown(nome que eu quiser dar a animação){
                            0%{
                                opacity:0;
                                transform:TranslateY(-15px);
                            }

                            100%{
                                opacity:1;
                                transform:translateY(0);
                            }
                        }

                        começa no o com 0% de opacidade e com isso ele vai caindo de cima -15px para 0 ele volta ao normal


                        Para fazer o botão tremer e muito simples basta usar uma animation

                        #btnOpen:hover{
                            animation treme 0.5s
                            animation-iteration-count:infinite;
                        }

                        @keyframes treme{
                            0%{margin-left: 15px;}
                            10%{margin-left: 10px;}
                            25%{margin-left: 8px;}
                            50%{margin-left: 3px;}
                            75%{margin-right:5px;}
                            100%{margin-right:5px;}
                        }

PASSO QUARENTA E NOVE:

PASSO CINQUENTA:

PASSO CINQUENTA E UM:

PASSO CINQUENTA E TRES:

PASSO CINQUENTA: E QUATRO:

PASSO CINQUENTA E CINCO:

PASSO CINQUENTA E SEIS:

PASSO CINQUENTA E SETE:

PASSO CINQUENTA E OITO:

PASSO CINQUENTA E NOVE:

PASSO SESSENTA:

PASSO SESSENTA E UM:

PASSO SESSENTA E DOIS:

PASSO SESSENTA E TRES:

PASSO SESSENTA E QUATRO:

PASSO SESSENTA E CINCO:

PASSO SESSENTA E SEIS: