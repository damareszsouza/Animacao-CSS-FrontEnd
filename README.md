# Animacao-CSS-FrontEnd
Animação Css - Curso Programador Web - Praticas FrontEnd


Animações CSS
Animações CSS
CSS permite a animação de elementos HTML sem usar JavaScript ou Flash!

CSS
Neste capítulo, você aprenderá sobre as seguintes propriedades:

@keyframes
animation-name
animation-duration
animation-delay
animation-iteration-count
animation-direction
animation-timing-function
animation-fill-mode
animation
Suporte do navegador para animações
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a propriedade.

Property					
@keyframes	43.0	10.0	16.0	9.0	30.0
animation-name	43.0	10.0	16.0	9.0	30.0
animation-duration	43.0	10.0	16.0	9.0	30.0
animation-delay	43.0	10.0	16.0	9.0	30.0
animation-iteration-count	43.0	10.0	16.0	9.0	30.0
animation-direction	43.0	10.0	16.0	9.0	30.0
animation-timing-function	43.0	10.0	16.0	9.0	30.0
animation-fill-mode	43.0	10.0	16.0	9.0	30.0
animation	43.0	10.0	16.0	9.0	30.0
O que são animações CSS?
Uma animação permite que um elemento mude gradualmente de um estilo para outro.

Você pode alterar quantas propriedades CSS quiser, quantas vezes quiser.

Para usar a animação CSS, você deve primeiro especificar alguns quadros-chave para a animação.

Os quadros-chave contêm os estilos que o elemento terá em determinados momentos.

A regra @keyframes
Quando você especifica estilos CSS dentro da @keyframes regra, a animação mudará gradualmente do estilo atual para o novo estilo em determinados momentos.

Para que uma animação funcione, você deve vincular a animação a um elemento.

O exemplo a seguir vincula a animação "exemplo" ao elemento <div>. A animação durará 4 segundos e mudará gradualmente a cor de fundo do elemento <div> de "vermelho" para "amarelo":

Exemplo
/* The animation code */
@keyframes example {
  from {background-color: red;}
  to {background-color: yellow;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}
Observação: a animation-durationpropriedade define quanto tempo uma animação deve levar para ser concluída. Se a animation-durationpropriedade não for especificada, nenhuma animação ocorrerá, pois o valor padrão é 0s (0 segundos). 

No exemplo acima, especificamos quando o estilo será alterado usando as palavras-chave "from" e "to" (que representam 0% (início) e 100% (completo)).

Também é possível usar por cento. Ao usar a porcentagem, você pode adicionar quantas alterações de estilo quiser.

O exemplo a seguir mudará a cor de fundo do elemento <div> quando a animação estiver 25% concluída, 50% concluída e novamente quando a animação estiver 100% concluída:

Exemplo
/* The animation code */
@keyframes example {
  0%   {background-color: red;}
  25%  {background-color: yellow;}
  50%  {background-color: blue;}
  100% {background-color: green;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}
O exemplo a seguir mudará a cor de fundo e a posição do elemento <div> quando a animação estiver 25% concluída, 50% concluída e novamente quando a animação estiver 100% concluída:

Exemplo
/* The animation code */
@keyframes example {
  0%   {background-color:red; left:0px; top:0px;}
  25%  {background-color:yellow; left:200px; top:0px;}
  50%  {background-color:blue; left:200px; top:200px;}
  75%  {background-color:green; left:0px; top:200px;}
  100% {background-color:red; left:0px; top:0px;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}
ADVERTISEMENT

ADVERTISEMENT

Atrasar uma Animação
A animation-delaypropriedade especifica um atraso para o início de uma animação.

O exemplo a seguir tem um atraso de 2 segundos antes de iniciar a animação:

Exemplo
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-delay: 2s;
}
Valores negativos também são permitidos. Se estiver usando valores negativos, a animação começará como se já estivesse sendo reproduzida por N segundos.

No exemplo a seguir, a animação iniciará como se já estivesse sendo reproduzida por 2 segundos:

Exemplo
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-delay: -2s;
}
Definir quantas vezes uma animação deve ser executada
A animation-iteration-countpropriedade especifica o número de vezes que uma animação deve ser executada.

O exemplo a seguir executará a animação 3 vezes antes de parar:

Exemplo
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: 3;
}
O exemplo a seguir usa o valor "infinito" para fazer a animação continuar para sempre:

Exemplo
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: infinite;
}
Executar animação na direção reversa ou ciclos alternativos
A animation-directionpropriedade especifica se uma animação deve ser reproduzida para frente, para trás ou em ciclos alternados.

A propriedade animation-direction pode ter os seguintes valores:

normal- A animação é reproduzida normalmente (para frente). Isso é padrão
reverse- A animação é reproduzida na direção inversa (para trás)
alternate - A animação é reproduzida primeiro para frente e depois para trás
alternate-reverse- A animação é reproduzida primeiro para trás e depois para a frente
O exemplo a seguir executará a animação na direção inversa (para trás):

Exemplo
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-direction: reverse;
}
O exemplo a seguir usa o valor "alternate" para fazer a animação avançar primeiro e depois retroceder:

Exemplo
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: 2;
  animation-direction: alternate;
}
O exemplo a seguir usa o valor "alternate-reverse" para fazer a animação rodar primeiro para trás e depois para frente:

Exemplo
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: 2;
  animation-direction: alternate-reverse;
}
Especifique a curva de velocidade da animação
A animation-timing-functionpropriedade especifica a curva de velocidade da animação.

A propriedade animation-timing-function pode ter os seguintes valores:

ease- Especifica uma animação com início lento, rápido e final lento (este é o padrão)
linear- Especifica uma animação com a mesma velocidade do início ao fim
ease-in- Especifica uma animação com início lento
ease-out- Especifica uma animação com final lento
ease-in-out- Especifica uma animação com início e fim lentos
cubic-bezier(n,n,n,n)- Permite definir seus próprios valores em uma função cúbica-bezier
O exemplo a seguir mostra algumas das diferentes curvas de velocidade que podem ser usadas:

Exemplo
#div1 {animation-timing-function: linear;}
#div2 {animation-timing-function: ease;}
#div3 {animation-timing-function: ease-in;}
#div4 {animation-timing-function: ease-out;}
#div5 {animation-timing-function: ease-in-out;}
Especifique o modo de preenchimento para uma animação
As animações CSS não afetam um elemento antes da reprodução do primeiro quadro-chave ou após a reprodução do último quadro-chave. A propriedade de modo de preenchimento de animação pode substituir esse comportamento.

A animation-fill-modepropriedade especifica um estilo para o elemento de destino quando a animação não está sendo reproduzida (antes de começar, depois de terminar ou ambos).

A propriedade animation-fill-mode pode ter os seguintes valores:

none- Valor padrão. A animação não aplicará nenhum estilo ao elemento antes ou depois de sua execução
forwards- O elemento manterá os valores de estilo definidos pelo último quadro-chave (depende da direção da animação e da contagem de iterações da animação)
backwards- O elemento obterá os valores de estilo definidos pelo primeiro quadro-chave (depende da direção da animação) e os reterá durante o período de atraso da animação
both- A animação seguirá as regras tanto para frente quanto para trás, estendendo as propriedades da animação em ambas as direções
O exemplo a seguir permite que o elemento <div> mantenha os valores de estilo do último quadro-chave quando a animação terminar:

Exemplo
div {
  width: 100px;
  height: 100px;
  background: red;
  position: relative;
  animation-name: example;
  animation-duration: 3s;
  animation-fill-mode: forwards;
}
O exemplo a seguir permite que o elemento <div> obtenha os valores de estilo definidos pelo primeiro quadro-chave antes do início da animação (durante o período de atraso da animação):

Exemplo
div {
  width: 100px;
  height: 100px;
  background: red;
  position: relative;
  animation-name: example;
  animation-duration: 3s;
  animation-delay: 2s;
  animation-fill-mode: backwards;
}
O exemplo a seguir permite que o elemento <div> obtenha os valores de estilo definidos pelo primeiro quadro-chave antes do início da animação e mantenha os valores de estilo do último quadro-chave quando a animação terminar:

Exemplo
div {
  width: 100px;
  height: 100px;
  background: red;
  position: relative;
  animation-name: example;
  animation-duration: 3s;
  animation-delay: 2s;
  animation-fill-mode: both;
}
Propriedade abreviada de animação
O exemplo abaixo usa seis das propriedades de animação:

Exemplo
div {
  animation-name: example;
  animation-duration: 5s;
  animation-timing-function: linear;
  animation-delay: 2s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}
O mesmo efeito de animação acima pode ser obtido usando a animationpropriedade abreviada:

Exemplo
div {
  animation: example 5s linear 2s infinite alternate;
}
Teste-se com exercícios
Exercício:
Adicione uma animação de 2 segundos para o elemento <div>, que muda a cor de vermelho para azul. Chame a animação de "exemplo".

<estilo>
div {
  largura: 100px;
  altura: 100px;
  cor de fundo: vermelho;
  nome-da-animação:
;
  
: 2s;
}

@keyframes exemplo {
  de {
: vermelho;}
  para {
: azul;}
}
</estilo>

<corpo>
  <div>Isto é um div</div>
</body>

Iniciar o exercício

Propriedades de Animação CSS
A tabela a seguir lista a regra @keyframes e todas as propriedades de animação CSS:

Property	Description
@keyframes	Specifies the animation code
animation	A shorthand property for setting all the animation properties
animation-delay	Specifies a delay for the start of an animation
animation-direction	Specifies whether an animation should be played forwards, backwards or in alternate cycles
animation-duration	Specifies how long time an animation should take to complete one cycle
animation-fill-mode	Specifies a style for the element when the animation is not playing (before it starts, after it ends, or both)
animation-iteration-count	Specifies the number of times an animation should be played
animation-name	Specifies the name of the @keyframes animation
animation-play-state	Specifies whether the animation is running or paused
animation-timing-function	Specifies the speed curve of the animation


Regra CSS @keyframes

Exemplo
Faça um elemento se mover gradualmente 200px para baixo:

@keyframes mymove {
  from {top: 0px;}
  to {top: 200px;}
}
Mais exemplos de "Experimente você mesmo" abaixo.

Definição e Uso
A @keyframesregra especifica o código de animação.

A animação é criada mudando gradualmente de um conjunto de estilos CSS para outro.

Durante a animação, você pode alterar o conjunto de estilos CSS várias vezes.

Especifique quando a mudança de estilo acontecerá em porcentagem ou com as palavras-chave "from" e "to", que é o mesmo que 0% e 100%. 0% é o início da animação, 100% é quando a animação está completa.

Dica: Para melhor suporte ao navegador, você deve sempre definir os seletores 0% e 100%.

Nota: Use as propriedades de animação para controlar a aparência da animação e também para vincular a animação aos seletores.

Observação: a regra !important é ignorada em um quadro-chave (veja o último exemplo nesta página).

Suporte do navegador
Os números na tabela especificam a primeira versão do navegador totalmente compatível com a regra.

Números seguidos por -webkit-, -moz- ou -o- especificam a primeira versão que funcionou com um prefixo.

Property					
@keyframes	43.0
4.0 -webkit-	10.0	16.0
5.0 -moz-	9.0
4.0 -webkit-	30.0
15.0 -webkit-
12.0 -o-
ANÚNCIO

ANÚNCIO

Sintaxe CSS
@keyframes animationname {keyframes-selector {css-styles;}}
Valores de propriedade
Value	Description
animationname	Required. Defines the name of the animation.
keyframes-selector	Required. Percentage of the animation duration.
Legal values:

0-100%
from (same as 0%)
to (same as 100%)

Note: You can have many keyframes-selectors in one animation.

css-styles	Required. One or more legal CSS style properties
Mais exemplos
Exemplo
Adicione muitos seletores de quadro-chave em uma animação:

@keyframes mymove {
  0%   {top: 0px;}
  25%  {top: 200px;}
  50%  {top: 100px;}
  75%  {top: 200px;}
  100% {top: 0px;}
}
Exemplo
Mude muitos estilos CSS em uma animação:

@keyframes mymove {
  0%   {top: 0px; background: red; width: 100px;}
  100% {top: 200px; background: yellow; width: 300px;}
}
Exemplo
Muitos seletores de quadro-chave com muitos estilos CSS:

@keyframes mymove {
  0%   {top: 0px; left: 0px; background: red;}
  25%  {top: 0px; left: 100px; background: blue;}
  50%  {top: 100px; left: 100px; background: yellow;}
  75%  {top: 100px; left: 0px; background: green;}
  100% {top: 0px; left: 0px; background: red;}
}
Exemplo
Observação: a regra !important é ignorada em um quadro-chave:

@keyframes myexample {
  from {top: 0px;}
  50%  {top: 100px !important;} /* ignored */
  to   {top: 200px;}
}

Propriedade de animação CSS

Exemplo
Vinculando uma animação a um elemento <div>, usando a propriedade abreviada:

div {
  animation: mymove 5s infinite;
}
Definição e Uso
A animationpropriedade é uma propriedade abreviada para:

nome da animação
duração da animação
função de tempo de animação
atraso de animação
contagem de iterações de animação
animação-direção
modo de preenchimento de animação
animação-play-state
Nota: Sempre especifique a propriedade de duração da animação , caso contrário, a duração é 0 e nunca será reproduzida.


Valor padrão:	nenhum 0 facilidade 0 1 normal nenhum em execução
Herdado:	não
Animatável:	não. Leia sobre animável
Versão:	CSS3
Sintaxe JavaScript:	objeto .style.animation="meumove 5s infinito"
Suporte do navegador
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a propriedade.

Números seguidos por -webkit-, -moz- ou -o- especificam a primeira versão que funcionou com um prefixo.

Property					
animation	43.0
4.0 -webkit-	10.0	16.0
5.0 -moz-	9.0
4.0 -webkit-	30.0
15.0 -webkit-
12.0 -o-
ANÚNCIO

ANÚNCIO

Sintaxe CSS
animation: name duration timing-function delay iteration-count direction fill-mode play-state;
Valores de propriedade
Value	Description
animation-name	Specifies the name of the keyframe you want to bind to the selector
animation-duration	Specifies how many seconds or milliseconds an animation takes to complete
animation-timing-function	Specifies the speed curve of the animation
animation-delay	Specifies a delay before the animation will start
animation-iteration-count	Specifies how many times an animation should be played
animation-direction	Specifies whether or not the animation should play in reverse on alternate cycles
animation-fill-mode	Specifies what values are applied by the animation outside the time it is executing
animation-play-state	Specifies whether the animation is running or paused
initial	Sets this property to its default value. Read about initial
inherit	Inherits this property from its parent element. Read about inherit

Páginas Relacionadas

Propriedade do nome da animação CSS

Exemplo
Especifique um nome para a animação @keyframes:

div {
  animation-name: mymove;
}
Definição e Uso
A animation-namepropriedade especifica um nome para a animação @keyframes .

Valor padrão:	nenhum
Herdado:	não
Animatável:	não. Leia sobre animável
Versão:	CSS3
Sintaxe JavaScript:	objeto .style.animationName="myNEWmove"
Suporte do navegador
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a propriedade.

Números seguidos por -webkit-, -moz- ou -o- especificam a primeira versão que funcionou com um prefixo.

Property					
animation-name	43.0
4.0 -webkit-	10.0	16.0
5.0 -moz-	9.0
4.0 -webkit-	30.0
15.0 -webkit-
12.0 -o-
Sintaxe CSS
animation-name: keyframename|none|initial|inherit;
Valores de propriedade
Value	Description
keyframename	Specifies the name of the keyframe you want to bind to the selector
none	Default value. Specifies that there will be no animation (can be used to override animations coming from the cascade)
initial	Sets this property to its default value. Read about initial	
inherit	Inherits this property from its parent element. Read about inherit	


Propriedade CSS de duração da animação

Exemplo
Especifique que a animação deve completar um ciclo em 3 segundos:

div {
  animation-duration: 3s;
}
Definição e Uso
A animation-durationpropriedade define quanto tempo uma animação deve levar para completar um ciclo.

Valor padrão:	0
Herdado:	não
Animatável:	não. Leia sobre animável
Versão:	CSS3
Sintaxe JavaScript:	objeto .style.animationDuration="3s"
Suporte do navegador
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a propriedade.

Números seguidos por -webkit-, -moz- ou -o- especificam a primeira versão que funcionou com um prefixo.

Property					
animation-duration	43.0
3.0 -webkit-	10.0	16.0
5.0 -moz-	9.0
4.0 -webkit-	30.0
15.0 -webkit-
12.0 -o-
Sintaxe CSS
animation-duration: time|initial|inherit;
Valores de propriedade
Value	Description	Demo
time	Specifies the length of time an animation should take to complete one cycle. This can be specified in seconds or milliseconds. Default value is 0, which means that no animation will occur	
initial	Sets this property to its default value. Read about initial	
inherit	Inherits this property from its parent element. Read about inherit	


Propriedade de função de temporização de animação CSS

Exemplo
Reproduza uma animação com a mesma velocidade do começo ao fim:

div {
  animation-timing-function: linear;
}
Mais exemplos de "Experimente você mesmo" abaixo.

Definição e Uso
O animation-timing-functionespecifica a curva de velocidade de uma animação.

A curva de velocidade define o TEMPO que uma animação usa para mudar de um conjunto de estilos CSS para outro.

A curva de velocidade é usada para fazer as mudanças suavemente.

Valor padrão:	facilidade
Herdado:	não
Animatável:	não. Leia sobre animável
Versão:	CSS3
Sintaxe JavaScript:	objeto .style.animationTimingFunction="linear"
Suporte do navegador
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a propriedade.

Números seguidos por -webkit-, -moz- ou -o- especificam a primeira versão que funcionou com um prefixo.

Property					
animation-timing-function	43.0
4.0 -webkit-	10.0	16.0
5.0 -moz-	9.0
4.0 -webkit-	30.0
15.0 -webkit-
12.0 -o-
ANÚNCIO

Sintaxe CSS
animation-timing-function: linear|ease|ease-in|ease-out|ease-in-out|step-start|step-end|steps(int,start|end)|cubic-bezier(n,n,n,n)|initial|inherit;
A função de temporização da animação usa uma função matemática, chamada curva cúbica de Bezier, para fazer a curva de velocidade. Você pode usar seus próprios valores nesta função ou usar um dos valores predefinidos:
Valores de propriedade
Value	Description	Demo
linear	The animation has the same speed from start to end	
ease	Default value. The animation has a slow start, then fast, before it ends slowly	
ease-in	The animation has a slow start	
ease-out	The animation has a slow end	
ease-in-out	The animation has both a slow start and a slow end	
step-start	Equivalent to steps(1, start)	
step-end	Equivalent to steps(1, end)	
steps(int,start|end)	Specifies a stepping function, with two parameters. The first parameter specifies the number of intervals in the function. It must be a positive integer (greater than 0). The second parameter, which is optional, is either the value "start" or "end", and specifies the point at which the change of values occur within the interval. If the second parameter is omitted, it is given the value "end"	
cubic-bezier(n,n,n,n)	Define your own values in the cubic-bezier function
Possible values are numeric values from 0 to 1	
initial	Sets this property to its default value. Read about initial	
inherit	Inherits this property from its parent element. Read about inherit	
Dica: experimente os diferentes valores na seção "Mais exemplos" abaixo.

Mais exemplos
Exemplo
Para entender melhor os diferentes valores da função de temporização;
Aqui estão cinco elementos <div> diferentes com cinco valores diferentes:

#div1 {animation-timing-function: linear;}
#div2 {animation-timing-function: ease;}
#div3 {animation-timing-function: ease-in;}
#div4 {animation-timing-function: ease-out;}
#div5 {animation-timing-function: ease-in-out;}
Exemplo
Igual ao exemplo acima, mas as curvas de velocidade são definidas com a função cubic-bezier:

#div1 {animation-timing-function: cubic-bezier(0,0,1,1);}
#div2 {animation-timing-function: cubic-bezier(0.25,0.1,0.25,1);}
#div3 {animation-timing-function: cubic-bezier(0.42,0,1,1);}
#div4 {animation-timing-function: cubic-bezier(0,0,0.58,1);}
#div5 {animation-timing-function: cubic-bezier(0.42,0,0.58,1);}


Propriedade de atraso de animação CSS

Exemplo
Inicie a animação após 2 segundos:

div {
  animation-delay: 2s;
}
Mais exemplos de "Experimente você mesmo" abaixo.

Definição e Uso
A animation-delaypropriedade especifica um atraso para o início de uma animação.

O valor do atraso da animação é definido em segundos (s) ou milissegundos (ms).

Valor padrão:	0s
Herdado:	não
Animatável:	não. Leia sobre animável
Versão:	CSS3
Sintaxe JavaScript:	objeto .style.animationDelay="1s"
Suporte do navegador
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a propriedade.

Números seguidos por -webkit-, -moz- ou -o- especificam a primeira versão que funcionou com um prefixo.

Property					
animation-delay	43.0
4.0 -webkit-	10.0	16.0
5.0 -moz-	9.0
4.0 -webkit-	30.0
15.0 -webkit-
12.0 -o-
ANÚNCIO

ANÚNCIO

Sintaxe CSS
animation-delay: time|initial|inherit;
Valores de propriedade
Value	Description	Demo
time	Optional. Defines the number of seconds (s) or milliseconds (ms) to wait before the animation will start. Default value is 0. Negative values are allowed. If you use negative values, the animation will start as if it had already been playing for N seconds/milliseconds.	
initial	Sets this property to its default value. Read about initial	
inherit	Inherits this property from its parent element. Read about inherit	
Mais exemplos
Exemplo
Usando valores negativos. Aqui, a animação começará como se já estivesse tocando por 2 segundos:

div {
  animation-delay: -2s;
}

Propriedade CSS animation-iteration-count

Exemplo
Reproduza a animação duas vezes:

div {
  animation-iteration-count: 2;
}
Mais exemplos de "Experimente você mesmo" abaixo.

Definição e Uso
A animation-iteration-countpropriedade especifica o número de vezes que uma animação deve ser reproduzida.

Valor padrão:	1
Herdado:	não
Animatável:	não. Leia sobre animável
Versão:	CSS3
Sintaxe JavaScript:	objeto .style.animationIterationCount="infinito"
Suporte do navegador
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a propriedade.

Números seguidos por -webkit-, -moz- ou -o- especificam a primeira versão que funcionou com um prefixo.

Property					
animation-iteration-count	43.0
4.0 -webkit-	10.0	16.0
5.0 -moz-	9.0
4.0 -webkit-	30.0
15.0 -webkit-
12.0 -o-
ANÚNCIO

Sintaxe CSS
animation-iteration-count: number|infinite|initial|inherit;
Valores de propriedade
Value	Description	Demo
number	A number that defines how many times an animation should be played. Default value is 1	
infinite	Specifies that the animation should be played infinite times (for ever)	
initial	Sets this property to its default value. Read about initial	
inherit	Inherits this property from its parent element. Read about inherit	
Mais exemplos
Exemplo
Jogue a animação para sempre:

div {
  animation-iteration-count: infinite;
}

Propriedade de direção de animação CSS

Exemplo
Reproduza a animação primeiro para frente e depois para trás:

div {
  animation-direction: alternate;
}
Mais exemplos de "Experimente você mesmo" abaixo.

Definição e Uso
A animation-directionpropriedade define se uma animação deve ser reproduzida para frente, para trás ou em ciclos alternados.

Valor padrão:	normal
Herdado:	não
Animatável:	não. Leia sobre animável
Versão:	CSS3
Sintaxe JavaScript:	objeto .style.animationDirection="reverse"
Suporte do navegador
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a propriedade.

Números seguidos por -webkit-, -moz- ou -o- especificam a primeira versão que funcionou com um prefixo.

Property					
animation-direction	43.0
4.0 -webkit-	10.0	16.0
5.0 -moz-	9.0
4.0 -webkit-	30.0
15.0 -webkit-
12.0 -o-
ANÚNCIO

ANÚNCIO

Sintaxe CSS
animation-direction: normal|reverse|alternate|alternate-reverse|initial|inherit;
Valores de propriedade
Value	Description	Demo
normal	Default value. The animation is played as normal (forwards)	
reverse	The animation is played in reverse direction (backwards)	
alternate	The animation is played forwards first, then backwards	
alternate-reverse	The animation is played backwards first, then forwards	
initial	Sets this property to its default value. Read about initial	
inherit	Inherits this property from its parent element. Read about inherit	
Mais exemplos
Exemplo
Reproduza a animação primeiro para trás e depois para frente:

div {
  animation-direction: alternate-reverse;
}
Exemplo
Reproduza a animação ao contrário:

div {
  animation-direction: reverse;
}

Propriedade de modo de preenchimento de animação CSS

Exemplo
Deixe o elemento <div> reter os valores de estilo do último quadro-chave quando a animação terminar:

div {
  animation-fill-mode: forwards;
}
Mais exemplos de "Experimente você mesmo" abaixo.

Definição e Uso
A animation-fill-modepropriedade especifica um estilo para o elemento quando a animação não está sendo reproduzida (antes de começar, depois de terminar ou ambos).

As animações CSS não afetam o elemento antes da reprodução do primeiro quadro-chave ou após a reprodução do último quadro-chave. A animation-fill-modepropriedade pode substituir esse comportamento.

Valor padrão:	nenhum
Herdado:	não
Animatável:	não. Leia sobre animável
Versão:	CSS3
Sintaxe JavaScript:	objeto .style.animationFillMode="forwards"
Suporte do navegador
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a propriedade.

Números seguidos por -webkit-, -moz- ou -o- especificam a primeira versão que funcionou com um prefixo.

Property					
animation-fill-mode	43.0
4.0 -webkit-	10.0	16.0
5.0 -moz-	9.0
4.0 -webkit-	30.0
15.0 -webkit-
12.1
12.0 -o-
ANÚNCIO

ANÚNCIO

Sintaxe CSS
animation-fill-mode: none|forwards|backwards|both|initial|inherit;
Valores de propriedade
Value	Description
none	Default value. Animation will not apply any styles to the element before or after it is executing
forwards	The element will retain the style values that is set by the last keyframe (depends on animation-direction and animation-iteration-count)
backwards	The element will get the style values that is set by the first keyframe (depends on animation-direction), and retain this during the animation-delay period
both	The animation will follow the rules for both forwards and backwards, extending the animation properties in both directions
initial	Sets this property to its default value. Read about initial
inherit	Inherits this property from its parent element. Read about inherit
Mais exemplos
Exemplo
Deixe o elemento <div> obter os valores de estilo definidos pelo primeiro quadro-chave antes do início da animação (durante o período de atraso da animação):

div {
  animation-fill-mode: backwards;
}
Exemplo
Deixe o elemento <div> obter os valores de estilo definidos pelo primeiro quadro-chave antes do início da animação e mantenha os valores de estilo do último quadro-chave quando a animação terminar:

div {animation-fill-mode: both;
}

propriedade CSS animation-play-state

Exemplo
Pausar uma animação:

div {
  animation-play-state: paused;
}
Mais exemplos de "Experimente você mesmo" abaixo.

Definição e Uso
A animation-play-statepropriedade especifica se a animação está em execução ou pausada.

Nota: Use esta propriedade em um JavaScript para pausar uma animação no meio de um ciclo.

Valor padrão:	correndo
Herdado:	não
Animatável:	não. Leia sobre animável
Versão:	CSS3
Sintaxe JavaScript:	objeto .style.animationPlayState="pausado"
Suporte do navegador
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a propriedade.

Números seguidos por -webkit-, -moz- ou -o- especificam a primeira versão que funcionou com um prefixo.

Property					
animation-play-state	43.0
4.0 -webkit-	10.0	16.0
5.0 -moz-	9.0
4.0 -webkit-	30.0
15.0 -webkit-
12.0 -o-
ANÚNCIO

Sintaxe CSS
animation-play-state: paused|running|initial|inherit;
Valores de propriedade
Value	Description	Demo
paused	Specifies that the animation is paused	
running	Default value. Specifies that the animation is running	
initial	Sets this property to its default value. Read about initial	
inherit	Inherits this property from its parent element. Read about inherit	


Palavra-chave inicial do CSS

Exemplo
Defina a cor do texto do elemento <div> para vermelho, mas mantenha a cor inicial para os elementos <h1>:

div {
  color: red;
}

h1 {
  color: initial;
}
Definição e Uso
A initialpalavra-chave é usada para definir uma propriedade CSS para seu valor padrão.

A initialpalavra-chave pode ser usada para qualquer propriedade CSS e em qualquer elemento HTML.

Versão:	CSS3
Sintaxe JavaScript:	objeto .estilo. propriedade ="inicial"
Suporte do navegador
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a palavra-chave inicial.

Keyword					
initial	1.0	12.0	19.0	1.2	15.0
Sintaxe CSS
property: initial;
Páginas Relacionadas
CSS herdar palavra-chave: herdar palavra-chave

CSS herdar palavra-chave

Exemplo
Defina a cor do texto para os elementos <span> como azul, exceto aqueles dentro dos elementos com class="extra":

span {
  color: blue;
}

.extra span {
  color: inherit;
}
Definição e Uso
A inheritpalavra-chave especifica que uma propriedade deve herdar seu valor de seu elemento pai.

A inheritpalavra-chave pode ser usada para qualquer propriedade CSS e em qualquer elemento HTML.

Versão:	CSS3
Sintaxe JavaScript:	objeto .estilo. propriedade ="herdar"
Suporte do navegador
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a palavra-chave herdada.

Keyword					
inherit	1.0	8.0 	1.0	1.0	4.0
Sintaxe CSS
property: inherit;
Páginas Relacionadas

Palavra-chave inicial do CSS

Exemplo
Defina a cor do texto do elemento <div> para vermelho, mas mantenha a cor inicial para os elementos <h1>:

div {
  color: red;
}

h1 {
  color: initial;
}
Definição e Uso
A initialpalavra-chave é usada para definir uma propriedade CSS para seu valor padrão.

A initialpalavra-chave pode ser usada para qualquer propriedade CSS e em qualquer elemento HTML.

Versão:	CSS3
Sintaxe JavaScript:	objeto .estilo. propriedade ="inicial"
Suporte do navegador
Os números na tabela especificam a primeira versão do navegador que suporta totalmente a palavra-chave inicial.

Keyword					
initial	1.0	12.0	19.0	1.2	15.0
Sintaxe CSS
property: initial;
