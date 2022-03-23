# Marcadores

Em seu CSS vc deve adicionar um recurso chamado marcadores. Eles servem para dizer que o código CSS dentro dele deve ser aplicado sob uma condição, que nesse caso é o
tamanho da tela em pixels. É interessante considerar 4 marcadores para seu código, pois eles cobrem a maioria das possibilidades de telas. são eles:

~~~HTML
@media screen and (min-width: 1200px){ /* CSS aqui */ }
@media screen and (min-width: 768px) and (max-width: 1200px){ /* CSS aqui */ }
@media screen and (min-width:480px) and (max-width: 768px){ /* CSS aqui */ }
@media screen and (max-width: 480px){ /* CSS aqui */ }
~~~

# Viewport

Viewport são um recurso importantíssimo quando falamos de acessar um site em um dispositivo móvel por um motivo bem simples: sem ele buga tudo! Mesmo que voce adicione
os marcadores, se um viewport não for adicionado o site fica bugado por um motivo bem bizarro: O touch screen dos celulares! Por isso voce deve adicionar o seguinte
HTML no seu Head:

~~~CSS 
<meta name="viewport" content="width=device-width, initial-scale=1" /> 
~~~

Além disso adicione também o seguinte marcador (esse é um pouco diferente, adicione exatamente como consta a seguir) no arquivo CSS global:

~~~CSS
@-ms-viewport{ width: device-width; }
~~~

# Medidas de tamanho

Algumas medidas do css, como pixels, são interessantes quando se está desenvolvendo algo que pode ser fixo, mas elas não se adequam a sites responsivos. Para elementos
como imagens, divs, alguns botões e coisas como quadros (uma div com bordas e conteúdo interno) é mais interessante usar a medida vw para width e vh para height pois elas estão relacionadas diretamente ao tamanho da tela (vw = viewport width; vh = viewport height). Pode ser interessante também colocar um max-width/max-height ou 
min-width/min-height para evitar distorção, como acontece bastante em imagens.
