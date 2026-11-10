# Breder Kart 🏁

Jogo de kart 3D da família Breder. Roda no navegador do celular e do computador.

## Arquivos

- `index.html`: o jogo inteiro. Ele só baixa o Three.js r128 e a fonte Baloo 2 da internet.
- `fotos/`: uma foto por pessoa, que aparece na tela inicial e no placar.

## Fotos

O nome de cada foto precisa ser **exatamente** igual ao nome abaixo, com maiúsculas e espaço:

| Pessoa | Arquivo |
|---|---|
| Anne Elise | `fotos/Anne Elise.jpg` |
| Alice | `fotos/Alice.jpg` |
| Cecília | `fotos/Cecília.jpg` |
| Laura | `fotos/Laura.jpg` |
| Luiza | `fotos/Luiza.jpg` |
| Davi | `fotos/Davi.jpg` |
| Sophia | `fotos/Sophia.jpg` |

Também funcionam `.jpeg`, `.png` e `.webp`, em minúsculas ou maiúsculas. Se a foto não existir, aparece o desenho em pixel art.

Fotos em pé (retrato) ficam melhores: a tela inicial corta a foto em 124×150 e o placar mostra num círculo.

## Publicar no GitHub Pages

1. Crie um repositório público no GitHub.
2. Clique em **Add file → Upload files** e envie o `index.html`.
3. Envie as fotos arrastando a pasta `fotos` inteira pro upload. Assim elas ficam dentro de `fotos/`.
4. Vá em **Settings → Pages** e escolha a branch `main`, pasta `/ (root)`.
5. Depois de 1 ou 2 minutos, o jogo fica no endereço https://c-breder.github.io/Breder-Kart/ .

O GitHub Pages diferencia maiúsculas de minúsculas no nome do arquivo: `alice.jpg` não é a mesma coisa que `Alice.jpg`.
