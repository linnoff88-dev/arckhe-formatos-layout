# formatos-layout

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![Formatos de vêÂ­deo](guia/assets/banner.jpg)](https://linnoff88-dev.github.io/

**ê°Å¸â¡Â§ê°Å¸â¡Â· [PortuguêÂªs](README.md) êÂ· ê°Å¸â¡Âºê°Å¸â¡Â¸ [English](README.en.md) êÂ· ê°Å¸â¡Âªê°Å¸â¡Â¸ [EspaêÂ±ol](README.es.md)**

## O que êÂ©

O formatos-layout êÂ© um catêÂ¡logo de formatos de vêÂ­deo para quem grava com um apresentador (avatar) e mostra conteêÂºdo junto: mapa, grêÂ¡fico, print ou foto. Cada formato tem um nome fixo, como Largo, Bolha ou Telejornal. Assim dêÂ¡ para pedir "monta no Bolha 9:16" sem explicar o layout de novo. Ele traz um script que monta o vêÂ­deo final a partir de dois arquivos, o vêÂ­deo do conteêÂºdo e o vêÂ­deo do apresentador. Para usar, basta ter o ffmpeg e o Python instalados.

## ê°Å¸ââ Guia de uso

Guia completo, com os 20 exemplos em vêÂ­deo: **https://linnoff88-dev.github.io/

## Os formatos

| 16:9 (horizontal) | 9:16 (vertical) |
|---|---|
| **Largo**: conteêÂºdo êÂ  esquerda, apresentador numa coluna êÂ  direita | **Faixa**: conteêÂºdo em cima, apresentador numa faixa embaixo |
| **Canto**: conteêÂºdo em tela cheia, rosto num quadro no canto | **Canto**: conteêÂºdo em tela cheia, rosto num quadro embaixo |
| **Bolha**: conteêÂºdo em tela cheia, rosto num cêÂ­rculo | **Bolha**: conteêÂºdo em tela cheia, rosto num cêÂ­rculo |
| **Telejornal**: apresentador em tela cheia nos trechos escolhidos | **Telejornal**: apresentador em tela cheia nos trechos escolhidos |
| **Dividido**: metade conteêÂºdo, metade apresentador | **Apresentador**: apresentador grande, conteêÂºdo num cartêÂ£o em cima |
| **Apresentador**: apresentador domina, conteêÂºdo num cartêÂ£o | **Viral**: cortes secos a cada 2 s, fecha no apresentador |
| **DocumentêÂ¡rio**: sêÂ³ voz sobre o conteêÂºdo, rosto no fim | **DocumentêÂ¡rio**: sêÂ³ voz sobre o conteêÂºdo, rosto no fim |
| **Aula**: conteêÂºdo em tela cheia, rosto pequeno no canto de cima | **Metade**: avatar grande na metade de baixo |
| | **Invertido**: avatar em cima, conteêÂºdo embaixo |
| | **Pergunta**: Faixa no gancho ê¢â â Canto ê¢â â avatar grande na pergunta |
| | **Empilhado**: conteêÂºdo / avatar / conteêÂºdo em 3 faixas |
| | **Personagem**: o personagem ocupa o vêÂ­deo inteiro |

Detalhes, quando usar cada um e exemplos: [FORMATOS.md](FORMATOS.md).

O [FORMATOS.md](FORMATOS.md) tambêÂ©m traz onde o avatar aparece em cada formato e **quais formatos cada projeto de vêÂ­deo do ARCKHê usa** (explicavideos, eventosextremospub, r7e, finviral, promoavatar, docflow e outros).

## Uso

```bash
./compor.sh --formato bolha --aspecto 16x9 --cena cena.mp4 --avatar avatar.mp4 --saida video.mp4
```

- `--cena`: vêÂ­deo do conteêÂºdo jêÂ¡ no aspecto final (1920êâ1080 ou 1080êâ1920).
- `--avatar`: vêÂ­deo 16:9 do apresentador, com a voz.
- OpêÂ§êÂµes: `--ss`/`--t` (trecho), `--trechos "0-4,30-34"` (Telejornal), `--fim 6` (DocumentêÂ¡rio), `--nome "..."` (plaquinha), `MUSICA=trilha.mp3`, `AV_CX`/`AV_CY` (centro do rosto).

Precisa de `ffmpeg`, Python 3 e Pillow. NêÂ£o usa GPU.

## LicenêÂ§a

MIT

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>