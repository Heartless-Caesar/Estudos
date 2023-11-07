# Realce de imagens

#### Definição

Técnicas que conseguem acentuar algumas das caraterísticas relevantes em imagens para uma aplicação específica.

Essas aplicações podem ser:

- Melhorar sua qualidade;
- Aumentar o contraste da imagem;
- Facilitar procedimentos adicionais como detecção da borda das regiões na imagem.

Alterar os valores dos pixels de uma imagem a fim de obter uma nova imagem, de melhor visualização é chamado de *Realce de imagens*.

*Realce de imagens* é utilizado principalmente para obter iamgens que sejam percebidas pelo sistema visual humano.


### Categoria de Realce

#### Realce Espacial

Considera uma imagem como um domínio espacial, ou seja, como funções de luminância/brilhância l(u, v) de cada pixel(u, v). É comum no uso do histograma nestas técnicas para analisar a distribuição de ocorrências de níveis de cinza/cores numa imagem e decidir os novos valores para cada pixel.

São também conhecidas por processamentos pontuais, ou pixel a pixel, pois elas são caracterizadas por processarem os pontos isoladamente.

### Histograma

Permite entender a distribuição da intensidade/cor e comparar com as distribuições de outras imagens.


---

# Filtros de Realce


#### Também chamados de **Filtros de Passa-Alta**


- O realce chamado *Sharpening* tem como objetivo destacar as transições de uma intensidade na imagem;
- Utiliza um tipo de máscara que tende a realçar as diferenças de níveis de cinza na imagem.


#### Analogias

- Filtro de média (suavização) <-> Integração
- Realce <-> Derivação

- As derivadas de uma função digital são definidas em termos de diferenças entre os pixels


---

- *Derivações* são proporcioanis ao grau de descontinuidade na imagem;
	- Enfatizam as regições de bordas e os ruídos;
	- Não enfatizam regiões constantes ou com variações de intensidade suaves.
	
- Filtros
	- Laplaciano;
	- Unsharp masking e highboost filtering;
	- Derivativos.
---

#### Filtro Laplaciano

- Utiliza derivadas de segunda ordem
	+ Resposta mais acentuada e detalhes finos como pontos isolados e linhas
- É um filtro isotrópico
	+ A resposta é independente da direção da descontinuidade na imagem em que o filtro é aplicado(invariante à rotação)
	
- Máscaras para o filtro Laplaciano
	+ Centro negativo: remove bordas exteriores;
	+ Centro positivo: remove bordas interiores.
	

O Filtro Laplaciano realça bordas ou descontinuidades na imagem, porém ameniza regiões com nível de cinza constante.
Vale notar que algumas imagens o fundo da mesma pode ser perdido assim sendo necessário reconstruir o mesmo, é feito utilizando a fórmula:


	g(x,y) = f(x,y) + c[🔺²f(x,y)]
	
 
 + *c* é uma constante
 	-  c = -1 se o centro da máscara é negativo
 	-  c = 1 caso contrário
 	

- Logo g(x,y) pode ser interpretado como a recuperação do fundo da imagem.


Como o Filtro Laplaciano é linear, existem máscaras que já combinam as duas operações:
- Realce + reconstrução do fundo da imagem


---

### Unsharp Masking (Máscara de nitidez) e FIltragem Highboost

Seja s(x, y) uma suavização da imagem f(x,y)

g mask(x, y) = f(x, y) - s(x, y)

g(x, y) = f(x, y) + g mask(x, y)

*Unsharp Masking (Máscara de nitidez)* e *Filtragem Highboost* são técnicas de processamento de imagem utilizadas para aumentar a nitidez e realçar os detalhes de uma imagem. Elas são comumente usadas em softwares de edição de imagem, como o Adobe Photoshop, para melhorar a qualidade das fotografias ou imagens.

#### Unsharp Masking (Máscara de nitidez)
A técnica de Unsharp Masking é uma das mais antigas e amplamente usadas para aumentar a nitidez em uma imagem. Ela funciona através dos seguintes passos:

- Criação da máscara: Uma cópia da imagem original é desfocada (geralmente usando um filtro gaussiano) para criar uma máscara de desfoque. Essa máscara contém as informações de contraste e detalhes perdidos na imagem original.

- Aplicação da máscara: A máscara de desfoque é então subtraída da imagem original. Essa subtração cria uma imagem que realça as diferenças de contraste, destacando os detalhes e as bordas.

- Ajuste de intensidade: O resultado da subtração é multiplicado por um fator de intensidade para controlar a quantidade de nitidez aplicada à imagem. Esse fator pode ser ajustado pelo usuário para alcançar o nível desejado de nitidez.

Unsharp Masking é uma técnica eficaz, mas é importante usá-la com moderação, pois o excesso de nitidez pode resultar em artefatos visuais e uma aparência pouco natural.

#### Filtragem Highboost

A Filtragem Highboost é uma variação da técnica de Unsharp Masking e também é usada para aumentar a nitidez em uma imagem. Ela funciona da seguinte maneira:

- Criação da máscara de realce: Em vez de criar uma máscara de desfoque como no Unsharp Masking, na Filtragem Highboost, a máscara de realce é criada diretamente. Essa máscara contém valores positivos no centro, representando os detalhes e bordas a serem realçados, e valores negativos na periferia, representando os detalhes a serem atenuados.

- Aplicação da máscara: A máscara de realce é aplicada à imagem original usando uma operação de convolução. Isso realça os detalhes da imagem, aumentando o contraste local e a nitidez.

A principal diferença entre a Filtragem Highboost e o Unsharp Masking está na criação da máscara. Enquanto o Unsharp Masking usa uma máscara de desfoque, a Filtragem Highboost cria uma máscara de realce diretamente, permitindo um controle mais preciso sobre o processo de realce de nitidez.

Ambas as técnicas são valiosas para melhorar a qualidade de imagens desfocadas ou com baixo contraste, mas é importante usá-las com cuidado para evitar resultados excessivamente processados ou artificiais.