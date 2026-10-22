# MinigameRars
Repositório criado para a confecção do jogo do de Introdução a Sistemas Computacionais.

Estrutura do Projeto
isaac/
│
├── main.s ........................ ÚNICO arquivo que você executa no RARS
│                                   (dá os .include em tudo e tem o loop principal)
│
├── config/
│   └── constantes.s .............. números fixos com nome (.eqm)
│                                   ex.: endereço do display, tamanho do tile
│                                   → usado por TODOS os arquivos
│
├── data/ ......................... só DADOS (imagens, mapas, notas). Nenhum código aqui
│   ├── sprites/
│   │   ├── isaac.data ............ pixels do personagem → lido por render.s
│   │   ├── inimigo1.data ......... → lido por render.s
│   │   ├── inimigo2.data ......... → lido por render.s
│   │   ├── chefe.data ............ → lido por render.s
│   │   └── tiro.data ............. → lido por render.s
│   ├── mapas/
│   │   ├── sala1.data ............ matriz de tiles → lida por cenario.s e colisao.s
│   │   ├── sala2.data
│   │   ├── sala3.data
│   │   └── sala_chefe.data ....... o 4º cenário
│   └── musica.data ............... notas e durações → lido por audio.s
│
├── src/ .......................... só CÓDIGO (cada arquivo = uma responsabilidade)
│   ├── input.s ................... lê o teclado
│   ├── jogador.s ................. posição, vidas, movimento, bomba
│   ├── tiro.s .................... projéteis
│   ├── inimigos.s ................ os 2 inimigos básicos
│   ├── chefe.s ................... o chefão
│   ├── colisao.s ................. quem bateu em quem
│   ├── cenario.s ................. sala atual, troca de sala, puzzle
│   ├── render.s .................. desenha tudo na tela
│   ├── hud.s ..................... desenha vidas/fase/power-up
│   ├── audio.s ................... toca música e efeitos
│   └── cheats.s .................. pular de fase na apresentação
│
├── tools/ ........................ programas auxiliares (não entram no jogo)
│   └── conversor de imagem → .data
│
└── docs/
    └── artigo/ ................... artigo em PDF (não entra no jogo)
