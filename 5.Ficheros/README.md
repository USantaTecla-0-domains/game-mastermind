# Mastermind. Requisitos Ficheros
Universo Santa Tecla  
[uSantaTecla@gmail.com](mailto:uSantaTecla@gmail.com)  
  
**Índice**

1. [Requisitos](#requisitos)
2. [Vista de Casos de Uso](#vista-de-casos-de-uso)  
   2.1. [Vista de Caso de Uso Start](#vista-de-caso-de-uso-start)  
   2.2. [Vista de Caso de Uso Open](#vista-de-cas-de-uso-open)  
   2.3. [Vista de Caso de Uso Propose](#vista-de-caso-de-uso-propose)  
   2.4. [Vista de Caso de Uso Undo](#vista-de-caso-de-uso-undo)  
   2.5. [Vista de Caso de Uso Redo](#vista-de-caso-de-uso-redo)  
   2.6. [Vista de Caso de Uso Exit](#vista-de-cas-de-uso-exit)  
   2.7. [Vista de Caso de Uso Save](#vista-de-cas-de-uso-save)  
   2.8. [Vista de Caso de Uso Resume](#vista-de-caso-de-uso-resume)  
   2.9. [Vista de Caso de Uso incluido ShowBoard](#vista-de-caso-de-uso-incluido-showboard)  
   2.10. [Prototipo de Interfaz](#prototipo-de-interfaz)  

## Requisitos  

| [Wiki](https://en.wikipedia.org/wiki/Mastermind_(board_game)) - [Youtube](https://www.youtube.com/watch?v=2-hTeg2M6GQ&ab_channel=ViciadosMesa)<br/> * _Funcionalidad: **Básica + Undo/Redo**_<br/>  * _Interfaz: **Gráfica y Texto**_<br/>  * _Distribución: **Standalone + Client/Server**_<br/>  * _Persistencia: **Ficheros**_<br/> | ![TicTacToe](./docs/images/mastermind.jpg) | 
| :------- | :------: |  

## Vista de Casos de Uso

| Diagrama de Actores y Casos de Uso | Diagrama de Contexto |
|---|---|
| ![Mastermind](./docs/diagrams/out/mastermind_usecases/mastermind_usecases.svg) | ![Mastermind](./docs/diagrams/out/mastermind_usecases/mastermind_states.svg) |  

## Vista de Caso de Uso Start
![Start](./docs/diagrams/out/mastermind_usecases/start_usecase.svg)

## Vista de Caso de Uso Open
![Open](./docs/diagrams/out/mastermind_usecases/open_usecase.svg)  

## Vista de Caso de Uso Propose
![Propose](./docs/diagrams/out/mastermind_usecases/propose_combination_usecase.svg)  

## Vista de Caso de Uso Undo
![Propose](./docs/diagrams/out/mastermind_usecases/undo_usecase.svg)  

## Vista de Caso de Uso Redo
![Propose](./docs/diagrams/out/mastermind_usecases/redo_usecase.svg)  

## Vista de Caso de Uso Exit
![Exit](./docs/diagrams/out/mastermind_usecases/exit_usecase.svg)  

## Vista de Caso de Uso Save
![Save](./docs/diagrams/out/mastermind_usecases/save_usecase.svg)  

## Vista de Caso de Uso Resume
![Resume](./docs/diagrams/out/mastermind_usecases/resume_usecase.svg)

## Vista de Caso de Uso incluido ShowBoard
![ShowBoard](./docs/diagrams/out/mastermind_usecases/show_board_usecase.svg)

### Prototipo de Interfaz  

```
----- MASTERMIND ---------
Choose one option ----
1. Start a new game
2. Open a saved game
1
0 attempt(s):
----- Choose one option ----
1. Propose Combination
2. Exit game
1
Propose a combination: rybc
1 attempt(s):
rybc --> 0 blacks and 3 whites
----- Choose one option ----
1. Propose Combination
2. Undo previous Proposal
3. Exit game
3
Do you want to save the game?? (y/n): y
Name: game1
Do you want to continue? (y/n): y



----- MASTERMIND ---------
---- Choose one option ----
1. Start a new game
2. Open a saved game
2
----- Choose one option ----
1. game1.mm
1
game1.mm
1 attempt(s):
rybc --> 0 blacks and 3 whites
----- Choose one option ----
1. Propose Combination
2. Exit game
1
Propose a combination: mybc
2 attempt(s):
rybc --> 0 blacks and 3 whites
mybc --> 0 blacks and 3 whites
----- Choose one option ----
1. Propose Combination
2. Undo previous Proposal
3. Exit game
1
Propose a combination: rmbc
3 attempt(s):
rybc --> 0 blacks and 3 whites
mybc --> 0 blacks and 3 whites
rmbc --> 0 blacks and 3 whites
----- Choose one option ----
1. Propose Combination
2. Undo previous Proposal
3. Exit game
1
Propose a combination: rymc
4 attempt(s):
rybc --> 0 blacks and 3 whites
mybc --> 0 blacks and 3 whites
rmbc --> 0 blacks and 3 whites
rymc --> 0 blacks and 3 whites
----- Choose one option ----
1. Propose Combination
2. Undo previous Proposal
3. Exit game
1
Propose a combination: rybm
5 attempt(s):
rybc --> 0 blacks and 3 whites
mybc --> 0 blacks and 3 whites
rmbc --> 0 blacks and 3 whites
rymc --> 0 blacks and 3 whites
rybm --> 1 blacks and 3 whites
----- Choose one option ----
1. Propose Combination
2. Undo previous Proposal
3. Exit game
1
Propose a combination: brym
6 attempt(s):
rybc --> 0 blacks and 3 whites
mybc --> 0 blacks and 3 whites
rmbc --> 0 blacks and 3 whites
rymc --> 0 blacks and 3 whites
rybm --> 1 blacks and 3 whites
brym --> 1 blacks and 3 whites
----- Choose one option ----
1. Propose Combination
2. Undo previous Proposal
3. Exit game
1
Propose a combination: ybrm
7 attempt(s):
rybc --> 0 blacks and 3 whites
mybc --> 0 blacks and 3 whites
rmbc --> 0 blacks and 3 whites
rymc --> 0 blacks and 3 whites
rybm --> 1 blacks and 3 whites
brym --> 1 blacks and 3 whites
ybrm --> 4 blacks and 0 whites
You've won!!! ;-)
Do you want to save the game?? (y/n): n
Do you want to continue? (y/n):
```

