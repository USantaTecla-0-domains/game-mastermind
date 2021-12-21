# Mastermind. Requisitos Undo/Redo
Universo Santa Tecla  
[uSantaTecla@gmail.com](mailto:uSantaTecla@gmail.com)  
  
**Índice**

1. [Requisitos](#requisitos)
2. [Vista de Casos de Uso](#vista-de-casos-de-uso)  
   2.1. [Vista de Caso de Uso Start](#vista-de-caso-de-uso-start)  
   2.2. [Vista de Caso de Uso Propose](#vista-de-caso-de-uso-propose)  
   2.3. [Vista de Caso de Uso Undo](#vista-de-caso-de-uso-undo)  
   2.4. [Vista de Caso de Uso Redo](#vista-de-caso-de-uso-redo)  
   2.5. [Vista de Caso de Uso Resume](#vista-de-caso-de-uso-resume)  
   2.6. [Vista de Caso de Uso incluido ShowBoard](#vista-de-caso-de-uso-incluido-showboard)  
   2.7. [Prototipo de Interfaz](#prototipo-de-interfaz)  
      2.7.1. [Partida ganada](#partida-ganada)  
      2.7.2. [Partida perdida](#partida-perdida)

## Requisitos  

| [Wiki](https://en.wikipedia.org/wiki/Mastermind_(board_game)) - [Youtube](https://www.youtube.com/watch?v=2-hTeg2M6GQ&ab_channel=ViciadosMesa)<br/> * _Funcionalidad: **Básica + Undo/Redo**_<br/>  * _Interfaz: **Gráfica y Texto**_<br/>  * _Distribución: **Standalone**_<br/>  * _Persistencia: **No**_<br/> | ![TicTacToe](./docs/images/mastermind.jpg) | 
| :------- | :------: |  

## Vista de Casos de Uso

| Diagrama de Actores y Casos de Uso | Diagrama de Contexto |
|---|---|
| ![Mastermind](./docs/diagrams/out/mastermind_usecases/mastermind_usecases.svg) | ![Mastermind](./docs/diagrams/out/mastermind_usecases/mastermind_states.svg) |  

## Vista de Caso de Uso Start
![Start](./docs/diagrams/out/mastermind_usecases/start_usecase.svg)

## Vista de Caso de Uso Propose
![Propose](./docs/diagrams/out/mastermind_usecases/propose_combination_usecase.svg)  

## Vista de Caso de Uso Undo
![Propose](./docs/diagrams/out/mastermind_usecases/undo_usecase.svg)  

## Vista de Caso de Uso Redo
![Propose](./docs/diagrams/out/mastermind_usecases/redo_usecase.svg)  

## Vista de Caso de Uso Resume
![Resume](./docs/diagrams/out/mastermind_usecases/resume_usecase.svg)

## Vista de Caso de Uso incluido ShowBoard
![ShowBoard](./docs/diagrams/out/mastermind_usecases/show_board_usecase.svg)

### Prototipo de Interfaz

#### Partida ganada
```
----- MASTERMIND -----

0 attempt(s): 
****
Propose a combination: rybgmc
Wrong proposed combination length
Propose a combination: rybÑ
Wrong colors, they must be: rgybmc
Propose a combination: rybv
Wrong colors, they must be: rgybmc
Propose a combination: rybc

1 attempt(s): 
****
rybc --> 1 blacks and 3 whites
Propose a combination: rbcy

2 attempt(s): 
****
rybc --> 1 blacks and 3 whites
rbcy --> 1 blacks and 3 whites
Propose a combination: rcyb

3 attempt(s): 
****
rybc --> 1 blacks and 3 whites
rbcy --> 1 blacks and 3 whites
rcyb --> 0 blacks and 4 whites
Propose a combination: yrbc

4 attempt(s): 
****
rybc --> 1 blacks and 3 whites
rbcy --> 1 blacks and 3 whites
rcyb --> 0 blacks and 4 whites
yrbc --> 0 blacks and 4 whites
Propose a combination: bcry

5 attempt(s): 
****
rybc --> 1 blacks and 3 whites
rbcy --> 1 blacks and 3 whites
rcyb --> 0 blacks and 4 whites
yrbc --> 0 blacks and 4 whites
bcry --> 1 blacks and 3 whites
Propose a combination: bycr

6 attempt(s): 
****
rybc --> 1 blacks and 3 whites
rbcy --> 1 blacks and 3 whites
rcyb --> 0 blacks and 4 whites
yrbc --> 0 blacks and 4 whites
bcry --> 1 blacks and 3 whites
bycr --> 4 blacks and 0 whites
You've won!!! ;-)
Do you want to continue? (y/n): 
```

#### Partida perdida

```
----- MASTERMIND -----

0 attempt(s): 
****
Propose a combination: rgby

1 attempt(s): 
****
rgby --> 1 blacks and 2 whites
Propose a combination: rgby

2 attempt(s): 
****
rgby --> 1 blacks and 2 whites
rgby --> 1 blacks and 2 whites
Propose a combination: bygr

3 attempt(s): 
****
rgby --> 1 blacks and 2 whites
rgby --> 1 blacks and 2 whites
bygr --> 2 blacks and 1 whites
Propose a combination: rbgy

4 attempt(s): 
****
rgby --> 1 blacks and 2 whites
rgby --> 1 blacks and 2 whites
bygr --> 2 blacks and 1 whites
rbgy --> 2 blacks and 1 whites
Propose a combination: ygbr

5 attempt(s): 
****
rgby --> 1 blacks and 2 whites
rgby --> 1 blacks and 2 whites
bygr --> 2 blacks and 1 whites
rbgy --> 2 blacks and 1 whites
ygbr --> 0 blacks and 3 whites
Propose a combination: grby

6 attempt(s): 
****
rgby --> 1 blacks and 2 whites
rgby --> 1 blacks and 2 whites
bygr --> 2 blacks and 1 whites
rbgy --> 2 blacks and 1 whites
ygbr --> 0 blacks and 3 whites
grby --> 0 blacks and 3 whites
Propose a combination: rgby

7 attempt(s): 
****
rgby --> 1 blacks and 2 whites
rgby --> 1 blacks and 2 whites
bygr --> 2 blacks and 1 whites
rbgy --> 2 blacks and 1 whites
ygbr --> 0 blacks and 3 whites
grby --> 0 blacks and 3 whites
rgby --> 1 blacks and 2 whites
Propose a combination: rgby

8 attempt(s): 
****
rgby --> 1 blacks and 2 whites
rgby --> 1 blacks and 2 whites
bygr --> 2 blacks and 1 whites
rbgy --> 2 blacks and 1 whites
ygbr --> 0 blacks and 3 whites
grby --> 0 blacks and 3 whites
rgby --> 1 blacks and 2 whites
rgby --> 1 blacks and 2 whites
Propose a combination: rgby

9 attempt(s): 
****
rgby --> 1 blacks and 2 whites
rgby --> 1 blacks and 2 whites
bygr --> 2 blacks and 1 whites
rbgy --> 2 blacks and 1 whites
ygbr --> 0 blacks and 3 whites
grby --> 0 blacks and 3 whites
rgby --> 1 blacks and 2 whites
rgby --> 1 blacks and 2 whites
rgby --> 1 blacks and 2 whites
Propose a combination: gbry

10 attempt(s): 
****
rgby --> 1 blacks and 2 whites
rgby --> 1 blacks and 2 whites
bygr --> 2 blacks and 1 whites
rbgy --> 2 blacks and 1 whites
ygbr --> 0 blacks and 3 whites
grby --> 0 blacks and 3 whites
rgby --> 1 blacks and 2 whites
rgby --> 1 blacks and 2 whites
rgby --> 1 blacks and 2 whites
gbry --> 0 blacks and 3 whites
You've lost!!! :-(
Do you want to continue? (y/n): 
```


