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