Easytris
========

A fork of the tetris game in [BSDgames](https://github.com/vattam/BSDGames.git)
to experiment with game play with different piece distributions.

This will drop roughly 30 pieces in a row that are the same piece, starting
with a piece that does not neatly tile. After those 30 pieces, it switches
to another piece to hammer you with. And then again. Piece three is the square,
neatly filling space, as a breather. 

But to keep you from getting complacent, there's a small chance of getting
something else each time.

This gameplay rule change seems to have potential, but I found that by piece
four it has speeded up too much to use with these controls. The original
code does not have very responsive input at speed. Upon further digging,
the BSDgames version originates in an IOCCC entry, so good game play was
clearly not part of the original goal. :-/

Eli the Bearded
Friday February 16 to Sunday February 18, 2018
