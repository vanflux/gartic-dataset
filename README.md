# Gartic Drawings Dataset

*Apenas para fins de estudos!*

Repositório para armazenar datasets do gartic.io gerados através de um scrapper.<br>
Talvez o bot seja tornado público no futuro, mas por enquanto apenas dados.<br>
O dataset contém 5366 partidas do gartic.io em português na categoria de alimentos.

A lista de partidas é armazenada em um JSON.

[Releases/Downloads](https://github.com/vanflux/gartic-dataset/releases)

Estrutura do JSON:
```ts
[
  {
    colorPercentages: [
      {
        color: { r: number, g: number, b: number, a: number },
        percentage: number (float [0.0-1.0])
      }
    ],
    drawingName: string,
    duration: number (millis),
    guesses: [
      { guess: string, time: number (millis relative to round start) }
    ],
    hints: [
      { earnedPoints: number, time: number (millis relative to round start) }
    ],
    usedTips: boolean,
    usersCount: number,
  }
]
```

Lista de cores possíveis (caso o usuário tenha usado cores diferentes no desenho é feita uma aproximação usando nearest-neighbour no resultado final do render):
```ts
{ r: 0, g: 0, b: 0},
{ r: 102, g: 102, b: 102},
{ r: 139, g: 0, b: 0},
{ r: 0, g: 139, b: 0},
{ r: 0, g: 0, b: 139},
{ r: 0, g: 139, b: 139},
{ r: 139, g: 139, b: 0},
{ r: 139, g: 69, b: 0},
{ r: 139, g: 10, b: 80},
{ r: 85, g: 26, b: 139},
{ r: 84, g: 139, b: 84},
{ r: 139, g: 105, b: 105},
{ r: 139, g: 123, b: 139},
{ r: 255, g: 255, b: 255},
{ r: 204, g: 204, b: 204},
{ r: 255, g: 0, b: 0},
{ r: 0, g: 255, b: 0},
{ r: 0, g: 0, b: 255},
{ r: 0, g: 255, b: 255},
{ r: 255, g: 255, b: 0},
{ r: 255, g: 127, b: 0},
{ r: 255, g: 20, b: 147},
{ r: 155, g: 48, b: 255},
{ r: 154, g: 255, b: 154},
{ r: 255, g: 193, b: 193},
{ r: 255, g: 225, b: 255}
```
