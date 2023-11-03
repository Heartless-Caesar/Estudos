Pixel *p* que possui coordenadas (x, y):

- Possui 4 vizinhos horizontais:

  $$\ND(p) = \{(x + 1, y + 1), (x - 1, y - 1), (x + 1, y + 1), (x - 1, y - 1)\}$$

- Possui 4 vizinhos verticais:

  $$N4(p) = \{(x + 1, y), (x - 1, y), (x, y + 1), (x, y - 1)\}$$

- A soma dos conjuntos verticais e horizontais define a 8-vizinhança:

  $$N8(p) = N4(p) + \ND(p)$$
