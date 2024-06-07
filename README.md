

sou estudante do jõao cardoso do santos 

![](https://media1.tenor.com/m/duzc65T041UAAAAC/ronaldo-al-nassr-alnassr.gif)

//variaveis da bolinha
let xBolinha = 100;
let yBolinha = 200;
let diametro = 20;
let raio = diametro / 2;

//variaveis do oponente 
 let xRaqueteOponente = 585;
 let yRaqueteOponente = 150;

//velocidade da bolinha
let velocidadeXBolinha = 6;
let velocidadeYBolinha = 6;

 //variáveis da raquete
let xRaquete = 5 
let yRaquete =150;
let raqueteComprimento = 10;
let raqueteAltura = 90;

//placar do jogo 
 let meusPontos = 0;
 let pontosDoOponente = 0;
 let colidiu = false;

    function setup() {
  createCanvas(600, 400);
}

function draw() {
  background(0);
  mostraBolinha();
  movimentaBolinha();
  verificaColisaoBorda();
  mostrtaRaquete(xRaquete, yRaquete);
  movimentaMinhaRaquete();
  rect (5,150,10,90);
  
}


function mostraBolinha(){
  circle(xBolinha,yBolinha,diametro);
}

function movimentaBolinha(){
  xBolinha += velocidadeXBolinha;
  yBolinha += velocidadeYBolinha;
}

function verificaColisaoBorda(){
   if(xBolinha + raio > width || xBolinha - raio < 0){
      velocidadeXBolinha *= -1;
  }
  if(yBolinha + raio > height || yBolinha - raio < 0){
      velocidadeYBolinha *= -1;
  }
