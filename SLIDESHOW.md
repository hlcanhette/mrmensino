# Atualizar as imagens

Coloque as imagens diretamente em `assets/slideshow/`. Os formatos aceitos sao
JPG, JPEG, PNG, WebP, GIF e AVIF. Nao e necessario editar o HTML nem as bolinhas.
Os arquivos aparecem em ordem de nome, considerando os numeros: slide-1,
slide-2, slide-10. Use numeros no inicio para controlar a ordem.

## Publicacao automatica

Uma unica vez, no repositorio do GitHub, abra Settings > Pages > Build and
deployment > Source e selecione GitHub Actions. Envie tambem os novos arquivos
deste projeto, incluindo `.github/workflows/pages.yml` e `scripts/`.

Depois disso, ao enviar alteracoes para main ou master, a publicacao gera a
lista atualizada a partir da pasta. Adicionar, remover ou renomear imagens
atualiza tanto os slides quanto as bolinhas. A pasta vazia oculta o slideshow;
uma unica imagem aparece sem bolinhas nem troca automatica.

## Visualizacao local

Depois de alterar a pasta, execute `node scripts/generate-slideshow.mjs` antes
de abrir `index.html`. O arquivo `assets/slideshow-images.js` e gerado, nao
precisa ser editado manualmente. O navegador nao consegue listar sozinho os
arquivos de uma pasta local ou do GitHub Pages.

A altura acompanha a proporcao original de cada imagem, sem cortes. As
bolinhas ficam abaixo, fora da imagem. Para evitar mudancas de altura ao
trocar slides, use imagens com a mesma proporcao, por exemplo 1600 x 900 px.
