# Breder Kart 

**Jogar:** https://c-breder.github.io/Breder-Kart/

Breder Kart é um jogo de corrida de kart editável, feito para a família. É um site de um arquivo só (`index.html`): roda no navegador do computador ou do celular, sem instalar nada.

- **Offline:** uma pessoa contra até 3 rivais controlados pelo jogo.
- **Online:** até 5 pessoas, cada uma no seu aparelho, em salas com link, com senha ou na sala aberta.
- **Editável:** dá para trocar as fotos, mudar os avatares e criar personagens novos mexendo só em textos e imagens.

---

## Arquivos do projeto

| Arquivo / pasta | O que é |
|---|---|
| `index.html` | o jogo inteiro (tela, personagens, pista, corrida, online) |
| `fotos/` | as fotos dos personagens |
| `peerjs.min.js` | biblioteca do modo online (PeerJS) |
| `README.md` | este guia |

---

## Como trocar as fotos

1. Escolha a foto. Funciona melhor se for quadrada e com o rosto no centro.
2. Dê ao arquivo exatamente o mesmo nome que aparece no campo `file` do personagem (veja a lista em "Como mudar os avatares"). Por exemplo, para a Cecília: `Cecília.jpeg`.
3. Extensões aceitas: `.jpg`, `.jpeg`, `.png` ou `.webp`. O jogo procura nessa ordem e usa a primeira que encontrar.
4. Coloque o arquivo na pasta `fotos/`. Para trocar uma foto, substitua o arquivo antigo pelo novo, com o mesmo nome.
5. Abra o `index.html` no navegador e confira. Se ainda aparecer a foto antiga, recarregue a página
6. Publique (veja "Como publicar as mudanças").

**Observação:** fotos muito grandes deixam o jogo lento para abrir no celular. Algo em torno de **512×512 pixels** é suficiente. **O site é público, então as fotos também ficam públicas.**


## Como mudar os avatares

Os personagens ficam numa lista chamada `CHARS`, no `index.html`, na seção **2. Personagens"**:

```js
const BROWN='#6b4226', BLOND='#e2b850', EYE_B='#6a3a20', EYE_G='#3f9a4e';
const CHARS = [
  {name:'Anne Elise', file:'Anne Elise', eye:EYE_B, hair:BROWN, shirt:'#ff6fae'},
  {name:'Luiza',      file:'Luiza',      eye:EYE_G, hair:BLOND, shirt:'#2f6fdb'},
  {name:'Davi',       file:'Davi',       eye:EYE_G, hair:BLOND, shirt:'#2f6fdb', boy:true},
  {name:'Julia',      file:'Julia',      eye:'#5a3a24', hair:'#6b4a2e', tip:'#d8b07a', shirt:'#8e44d6'},
  // ...
];
```

Cada linha entre `{ }` é **um personagem**.

### Os campos de cada personagem

| Campo | Obrigatório? | O que muda | Exemplo |
|---|---|---|---|
| `name` | sim | o nome que aparece no jogo | `name:'Alice'` |
| `file` | sim | o nome do arquivo da foto em `fotos/` (sem a extensão) | `file:'Alice'` |
| `hair` | sim | cor do cabelo | `hair:'#6b4226'` |
| `eye` | sim | cor dos olhos | `eye:'#3f9a4e'` |
| `shirt` | sim | cor da blusa | `shirt:'#ff8a2a'` |
| `tip` | não | cor das pontas do cabelo (luzes) | `tip:'#d8b07a'` |
| `boy` | não | corte de cabelo curto | `boy:true` |
| `curly` | não | cabelo cacheado | `curly:true` |
| `skin` | não | cor da pele (se não tiver, usa o tom padrão) | `skin:'#c68642'` |

Há atalhos de cor prontos na primeira linha: `BROWN` (castanho), `BLOND` (loiro), `EYE_B` (olho castanho) e `EYE_G` (olho verde). Dá para usar o atalho ou escrever a cor direto.

### As cores

As cores são escritas em hexadecimal, sempre entre aspas e começando com `#`: `'#RRGGBB'` (vermelho, verde e azul, de `00` a `ff`). Exemplos: `'#ff0000'` vermelho, `'#2f6fdb'` azul, `'#f4f4f4'` branco.

Para tirar a cor de uma foto: abra a foto no Paint, use o conta-gotas no cabelo ou no olho e veja o código da cor em "Editar cores". No navegador, também dá para pesquisar "color picker" e usar o seletor de cores do Google.

### Mudar um personagem

1. Abra o `index.html` num editor de texto (VS Code ou Bloco de Notas).
2. Procure o nome do personagem, por exemplo `name:'Laura'`.
3. Troque o que quiser **dentro das aspas** (as cores) ou acrescente um campo opcional, separado por vírgula. Por exemplo, para dar luzes no cabelo:

   ```js
   {name:'Laura', file:'Laura', eye:EYE_B, hair:BROWN, tip:'#e2b850', shirt:'#3cb35a'},
   ```

4. Salve e abra o `index.html` no navegador para conferir.

### Criar um personagem novo

1. Copie uma linha inteira da lista (do `{` até o `},`) e cole logo abaixo dela.
2. Troque o `name`, o `file` e as cores.
3. Se quiser foto, coloque em `fotos/` com o mesmo nome do `file`.


## Como publicar as mudanças

O jogo é publicado pelo GitHub Pages: tudo o que estiver no GitHub, na branch `main`, vira o site. Em alguns minutos o site atualiza. Nos celulares, pode ser preciso fechar e abrir o jogo de novo.

## Créditos

- **PeerJS** (`peerjs.min.js`), biblioteca do modo online: peerjs.com, licença MIT.
