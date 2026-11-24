# formatos-layout

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![Formatos de vÃ­deo](guia/assets/banner.jpg)](https://linnoff88-dev.github.io/

**ðŸ‡§ðŸ‡· [PortuguÃªs](README.md) Â· ðŸ‡ºðŸ‡¸ [English](README.en.md) Â· ðŸ‡ªðŸ‡¸ [EspaÃ±ol](README.es.md)**

## O que Ã©

O formatos-layout Ã© um catÃ¡logo de formatos de vÃ­deo para quem grava com um apresentador (avatar) e mostra conteÃºdo junto: mapa, grÃ¡fico, print ou foto. Cada formato tem um nome fixo, como Largo, Bolha ou Telejornal. Assim dÃ¡ para pedir "monta no Bolha 9:16" sem explicar o layout de novo. Ele traz um script que monta o vÃ­deo final a partir de dois arquivos, o vÃ­deo do conteÃºdo e o vÃ­deo do apresentador. Para usar, basta ter o ffmpeg e o Python instalados.

## ðŸ“– Guia de uso

Guia completo, com os 20 exemplos em vÃ­deo: **https://linnoff88-dev.github.io/

## Os formatos

| 16:9 (horizontal) | 9:16 (vertical) |
|---|---|
| **Largo**: conteÃºdo Ã  esquerda, apresentador numa coluna Ã  direita | **Faixa**: conteÃºdo em cima, apresentador numa faixa embaixo |
| **Canto**: conteÃºdo em tela cheia, rosto num quadro no canto | **Canto**: conteÃºdo em tela cheia, rosto num quadro embaixo |
| **Bolha**: conteÃºdo em tela cheia, rosto num cÃ­rculo | **Bolha**: conteÃºdo em tela cheia, rosto num cÃ­rculo |
| **Telejornal**: apresentador em tela cheia nos trechos escolhidos | **Telejornal**: apresentador em tela cheia nos trechos escolhidos |
| **Dividido**: metade conteÃºdo, metade apresentador | **Apresentador**: apresentador grande, conteÃºdo num cartÃ£o em cima |
| **Apresentador**: apresentador domina, conteÃºdo num cartÃ£o | **Viral**: cortes secos a cada 2 s, fecha no apresentador |
| **DocumentÃ¡rio**: sÃ³ voz sobre o conteÃºdo, rosto no fim | **DocumentÃ¡rio**: sÃ³ voz sobre o conteÃºdo, rosto no fim |
| **Aula**: conteÃºdo em tela cheia, rosto pequeno no canto de cima | **Metade**: avatar grande na metade de baixo |
| | **Invertido**: avatar em cima, conteÃºdo embaixo |
| | **Pergunta**: Faixa no gancho â†’ Canto â†’ avatar grande na pergunta |
| | **Empilhado**: conteÃºdo / avatar / conteÃºdo em 3 faixas |
| | **Personagem**: o personagem ocupa o vÃ­deo inteiro |

Detalhes, quando usar cada um e exemplos: [FORMATOS.md](FORMATOS.md).

O [FORMATOS.md](FORMATOS.md) tambÃ©m traz onde o avatar aparece em cada formato e **quais formatos cada projeto de vÃ­deo do ARCKHÉ usa** (explicavideos, eventosextremospub, r7e, finviral, promoavatar, docflow e outros).

## Uso

```bash
./compor.sh --formato bolha --aspecto 16x9 --cena cena.mp4 --avatar avatar.mp4 --saida video.mp4
```

- `--cena`: vÃ­deo do conteÃºdo jÃ¡ no aspecto final (1920Ã—1080 ou 1080Ã—1920).
- `--avatar`: vÃ­deo 16:9 do apresentador, com a voz.
- OpÃ§Ãµes: `--ss`/`--t` (trecho), `--trechos "0-4,30-34"` (Telejornal), `--fim 6` (DocumentÃ¡rio), `--nome "..."` (plaquinha), `MUSICA=trilha.mp3`, `AV_CX`/`AV_CY` (centro do rosto).

Precisa de `ffmpeg`, Python 3 e Pillow. NÃ£o usa GPU.

## LicenÃ§a

MIT

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>