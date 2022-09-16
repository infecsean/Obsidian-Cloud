# New EE I guess
---
Reasoning: Since Ontogenetic/Teleological algorithms is too broad to simply compare as two "types". At least that's how Im not confident in it. I saw some examples with topics comparing djikstra's algorithm and A* algorithm. 

Things i found from [this paper](https://publications.lib.chalmers.se/records/fulltext/256132/256132.pdf)
- How hard is the algorithm to implement?
- How many levels of abstraction does it use? 
- How easy is it to change or adjust it into something specific? 
- How difficult or easy is to use? For whom?
- How easy is it to mix with other algorithms?
- How handmade does it feel? I.e, is it easy to detect that a human did not build a specific level?
- How much variation does it allow? Can one easily see patterns?
- How well does it scale up or down?
And this from this [paper](https://repository.library.northeastern.edu/files/neu:m0455c71t/fulltext.pdf)
![[Screen Shot 2022-09-16 at 4.06.18 PM.png]]

### Algorithms to consider:
1. Wave Function Collapse Algorithm
- [Explained](https://robertheaton.com/2018/12/17/wavefunction-collapse-algorithm/)
- [Explained 2](https://www.boristhebrave.com/2020/04/13/wave-function-collapse-explained/)

Pros:
- Very nice well know well documented algorithm
Cons:
- Hard
- Might cause problem in evaluation cus of tile-based generation

2. Agent Based Algorithm
	- [Terrain Generation](https://ianparberry.com/research/terrain/)
	- Data Structure: Linear
	
	Pros:
	- Good i guess
	Cons:
	- HARD ASF

3. Cellular Automation
- [Level Generation](https://www.raywenderlich.com/2425-procedural-level-generation-in-games-using-a-cellular-automaton-part-1)
- Data Structure: Random

Example:
```
A well-known example of cellular automata to many game developers is [Conway’s Game of Life](http://en.wikipedia.org/wiki/Conway%27s_Game_of_Life "Conway's Game of Life"), which is a two-dimensional grid of cells with each cell in a state of either dead or alive. Four transition rules govern the grid:

1.  Any live cell with fewer than two live neighbors dies, as if caused by under-population.
2.  Any live cell with two or three live neighbors lives on to the next generation.
3.  Any live cell with more than three live neighbors dies, as if by overcrowding.
4.  Any dead cell with exactly three live neighbors becomes a live cell, as if by reproduction.
```

Pros:
- Good resource tutorial
Cons:
- The tutorial is in XCode

4. Binary Space Partioning | Binary Space Tree
- [Dungeon Generator|Medium](https://medium.com/@guribemontero/dungeon-generation-using-binary-space-trees-47d4a668e2d0)
- Data Structure: Tree

Example
- Doom used it to generate dungeons
