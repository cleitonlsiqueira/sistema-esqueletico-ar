# Sistema Esquelético — protótipo WebAR

Este pacote já usa o modelo branco do esqueleto.

## Arquivos

- index.html — experiência de realidade aumentada com MindAR
- marcador-teste.html — imagem provisória que a câmera reconhece
- viewer.html — visualizador 3D comum, sem câmera
- assets/esqueleto_branco_webAR.glb — modelo 3D preparado

## Teste rápido

A experiência AR NÃO deve ser aberta clicando diretamente no arquivo index.html.
Ela precisa ser servida por um servidor web. Para câmera em outro aparelho, o ideal é HTTPS.

### Opção recomendada: GitHub Pages

1. Crie um repositório no GitHub, por exemplo: sistema-esqueletico-ar
2. Envie todos os arquivos desta pasta mantendo a estrutura.
3. Em Settings > Pages, publique a branch principal.
4. Abra a URL HTTPS gerada no celular.
5. Permita o acesso à câmera.
6. Em outro computador/tablet, abra `marcador-teste.html`.
7. Aponte o celular para a imagem de teste.

Quando a imagem for reconhecida, o esqueleto branco deve aparecer e se projetar para a frente.

## Teste somente no computador

Se você tiver Python instalado:

    python -m http.server 8000

Depois abra:

    http://localhost:8000/viewer.html

Para testar câmera no próprio computador, localhost normalmente é aceito.
Para testar pelo celular conectado à rede local, HTTP por IP geralmente não basta para câmera;
use HTTPS/GitHub Pages.

## Quando o painel estiver pronto

Vamos:
1. fotografar o painel perfeitamente de frente;
2. compilar essa foto no MindAR Image Targets Compiler;
3. substituir o `imageTargetSrc` do `index.html`;
4. recalibrar posição, escala e profundidade do esqueleto;
5. adicionar interações nos ossos;
6. gerar o QR Code definitivo.

## Créditos do modelo 3D

"Human Skeleton 3D Model" — Dinendra Neyo
Licença: Creative Commons Attribution (CC BY)

A atribuição deve permanecer no projeto final.
