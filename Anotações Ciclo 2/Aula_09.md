### Pixel *p* que possui coordenadas (x, y):

- Possui 4 vizinhos horizontais:

  $$ND(p) = \{(x + 1, y + 1), (x - 1, y - 1), (x -1 1, y + 1), (x + 1, y - 1)\}$$
  
  
  *Estes correspondem aos pixels localizados nas diagonais do pixel de referência*
  

  			
  		x - 1, y + 1                  x + 1, y + 1
  			              x,y
  
        x - 1, y - 1			x + 1, y - 1

- Possui 4 vizinhos verticais:

  $$N4(p) = \{(x + 1, y), (x - 1, y), (x, y + 1), (x, y - 1)\}$$
  
  *Estes correspondem, a partir do ponto de origem, as duas casas diretamente ao lado do pixel e as casas acima e abaixo diretamente dele*
  
		            x,y+1

  			        |	

  		x - 1, y __  x,y __  x + 1, y
  			       
  			        |   

  			     x, y - 1
  

- A soma dos conjuntos verticais e horizontais define a 8-vizinhança:

  $$N8(p) = N4(p) + ND(p)$$




### Conectividade

**A conectividade é importante porque é ele que ajuda a definir as bordas, com isso há necessidade de determinar se são adjacentes**

* 4-conectividade: Pertence ao conjunto N4(p), ou seja, os vizinhos verticais, portanto pode haver conexão com os diretamente adjacentes a ele;

* 8-conectividade: Pertence ao conjunto N8(p), ou seja, os vizinhos horizontais,
portanto pode haver conexão com os diagonais a ele;

* m-conectividade: Também chamada de adjacência mista, é quando um pixel pode ser ligado a pixels tanto verticais quanto horizontais, ou seja os diretamente adjacentes e diagonais; desta forma é uma mistura de 4-conectividade e 8-conectividade em que a 4-conectividade deve ser priorizada;

Exemplo de m-conectividade:


		0 1 - 1
		  |
		
		0 1   0
		    \
		0 0   1 





No exemplo acima é possível verificar que o pixel "1" no ponto de origem possui 8-conectividade com o pixel da diagonal(horizontal), 4-conectividade com o diretamente adjacente a ele(vertical) e este pixel **x, y + 1** possui 4-conectividade com o pixel **x + 1, y + 1** visto que a 4-conectividade foi priorizada.


### Ruídos em Imagens

#### Definição

É uma degradação que ocorre aleatóriamente assim alterando o conteúdo da imagem.
Estas ocorrem devido ao fato de imagens reais sofrerem degradações durante seu processo de aqiusição, transmissão ou processamento. 
