# processamento_imagens

# Separação dos Canais de Cores

Neste código, a imagem é carregada utilizando a função cv2.imread(), que recebe o caminho para o arquivo de imagem como parâmetro.

Após carregar a imagem, os canais de cores (vermelho, verde e azul) são separados utilizando a função cv2.split(), que retorna uma lista contendo cada canal separadamente.

### Adição de Texto e Valores Médios

Para cada canal de cor (r, g, b), é utilizada a função cv2.putText() para adicionar um texto contendo o valor médio do canal na imagem. Essa função recebe como parâmetros a imagem do canal, o texto a ser adicionado, as coordenadas onde o texto será posicionado, a fonte, o tamanho do texto, a cor do texto e a espessura da linha.

O valor médio do canal é obtido utilizando a função cv2.mean(), que retorna uma tupla contendo a média dos valores de pixel de cada canal. Nesse caso, é utilizado cv2.mean(b)[0] para obter a média do canal azul, cv2.mean(g)[0] para obter a média do canal verde e cv2.mean(r)[0] para obter a média do canal vermelho.

### Exibição dos Canais de Cores

Por fim, cada canal de cor é exibido separadamente utilizando a função cv2.imshow(), que recebe como parâmetros o nome da janela de exibição e a imagem correspondente ao canal de cor.

# Média

### Carregamento da Imagem
Neste código, a imagem é carregada utilizando a função cv2.imread(), que recebe o caminho para o arquivo de imagem como parâmetro.

### Conversão para Tons de Cinza
A imagem carregada é convertida para tons de cinza utilizando a função cv2.cvtColor(). Essa função recebe como parâmetros a imagem de entrada e o código cv2.COLOR_BGR2GRAY, indicando que a conversão deve ser feita para tons de cinza.

### Aplicação do Filtro da Média
O filtro da média é aplicado na imagem em tons de cinza utilizando a função cv2.blur(). Essa função recebe como parâmetros a imagem de entrada e o tamanho do kernel do filtro, que neste caso é definido como (5,5).

# Mediana

## Carregamento da Imagem
Neste código, a imagem é carregada utilizando a função cv2.imread(), que recebe o caminho para o arquivo de imagem como parâmetro.

### Conversão para Tons de Cinza
A imagem carregada é convertida para tons de cinza utilizando a função cv2.cvtColor(). Essa função recebe como parâmetros a imagem de entrada e o código cv2.COLOR_BGR2GRAY, indicando que a conversão deve ser feita para tons de cinza.

### Aplicação do Filtro da Mediana
O filtro da mediana é aplicado na imagem em tons de cinza utilizando a função cv2.medianBlur(). Essa função recebe como parâmetros a imagem de entrada e o tamanho do kernel do filtro, que neste caso é definido como 5.

# Limiarização

### Carregamento da Imagem em Tons de Cinza
Neste código, a imagem é carregada diretamente em tons de cinza utilizando a função cv2.imread() com o parâmetro cv2.IMREAD_GRAYSCALE. Isso significa que a imagem será lida e convertida para tons de cinza durante o carregamento.

### Aplicação da Limiarização
A limiarização é aplicada na imagem em tons de cinza utilizando a função cv2.threshold(). Essa função recebe como parâmetros a imagem de entrada, o valor de limiar, o valor máximo a ser atribuído aos pixels acima do limiar (255, no caso de uma imagem preto e branco), e o método de limiarização (neste caso, cv2.THRESH_BINARY indica que pixels acima do limiar serão definidos como branco e pixels abaixo do limiar serão definidos como preto).

# Invertida

### Vertical
Inverte a imagem verticalmente utilizando a função cv2.flip(). O resultado é armazenado na variável img_invertida.
Mostra a imagem original e a imagem invertida verticalmente utilizando a função cv2.imshow(). Os títulos das janelas de exibição são "Imagem Original" e "Imagem Invertida", respectivamente.

### Horizontal
Nessa parte, o código realiza as mesmas etapas da seção anterior, porém inverte a imagem horizontalmente utilizando a função cv2.flip(). A imagem invertida horizontalmente é exibida na janela com título "Imagem Invertida".

Essas operações permitem visualizar as imagens originais e suas versões invertidas verticalmente e horizontalmente.

# 90 graus
Rotaciona a imagem em 90 graus no sentido horário utilizando a função cv2.rotate(). O resultado da rotação é armazenado na variável img_rotacionada.
Exibe a imagem original e a imagem rotacionada utilizando a função cv2.imshow(). As janelas de exibição são identificadas pelos títulos "Imagem original" e "Imagem rotacionada", respectivamente.

# Desfoque Gaussiano
Aplica o filtro de desfoque gaussiano na imagem utilizando a função cv2.GaussianBlur(). O filtro suaviza a imagem, reduzindo o ruído e os detalhes, e melhora a qualidade visual. A imagem resultante do filtro é armazenada na variável img_blur.

Exibe a imagem original e a imagem com o filtro de desfoque gaussiano aplicado utilizando a função cv2.imshow(). As janelas de exibição são identificadas pelos títulos "Imagem original" e "Imagem com filtro de desfoque gaussiano", respectivamente.

# Ajuste de Contraste
Aplica a equalização do histograma na imagem utilizando a função cv2.equalizeHist(). A equalização do histograma é uma técnica de processamento de imagem que redistribui os valores de intensidade da imagem de forma a melhorar o contraste e realçar os detalhes.

Exibe as imagens original e a imagem com a equalização do histograma aplicada utilizando a função cv2.imshow(). As janelas de exibição são identificadas pelos títulos "Imagem Original" e "Imagem com Equalização de Histograma", respectivamente.

# Ajuste de Brilho
Adiciona o valor 50 a cada pixel da imagem utilizando a função cv2.add(). Essa função realiza a operação de adição elemento a elemento entre dois arrays (no caso, a imagem img e uma matriz com todos os elementos iguais a 50), resultando em uma nova imagem com o brilho ajustado. A imagem resultante é armazenada na variável img_bright.

Exibe as imagens original e a imagem com o brilho ajustado utilizando a função cv2.imshow(). As janelas de exibição são identificadas pelos títulos "Imagem Original" e "Imagem com Brilho Ajustado", respectivamente.

 
