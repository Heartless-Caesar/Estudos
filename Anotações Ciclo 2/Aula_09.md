### Pixel *p* que possui coordenadas (x, y):

- Possui 4 vizinhos horizontais:

  $$ND(p) = \{(x + 1, y + 1), (x - 1, y - 1), (x -1 1, y + 1), (x + 1, y - 1)\}$$

- Possui 4 vizinhos verticais:

  $$N4(p) = \{(x + 1, y), (x - 1, y), (x, y + 1), (x, y - 1)\}$$
  
  *Estes correspondem, a partir do ponto de origem, as duas casas diretamente ao lado do pixel e as casas acima e abaixo diretamente dele*
  
		           x,y+1
  			       |	
  		x - 1, y   X,y -  x + 1, y
  			       |   
  			   x, y - 1
  

- A soma dos conjuntos verticais e horizontais define a 8-vizinhança:

  $$N8(p) = N4(p) + ND(p)$$


### Conectividade

**A conectividade é importante porque é ele que ajuda a definir as bordas, com isso há necessidade de determinar se são adjacentes**

* 4-conectividade: Pertence ao conjunto N4(p), ou seja, os vizinhos verticais.






