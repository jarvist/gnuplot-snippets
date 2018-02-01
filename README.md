# gnuplot-snippets
Snippets for rendering ~publication quality figures in GNUPLOT.

## Why gnuplot in 2018?

I know, I know. All the cool kids use Matplotlib. Gnuplot is old, cranky, and ugly by default. The thing is, I was a cool kid once. 

I've wrestled repeatedly with Matplotlib magics to make a publication quality figure; I've returned to ~6 month old scripts to find them rendering very differently; sometimes the low performance is an actual problem. So I have returned to gnuplot as my main plotter.

In this repository I will try and collate / collect my useful bits and bobs for plotting with gnuplot.

### 'gnuplot-render.gpt' 

This is a 'function in a file' (bit of a hack, but it works). 
The idea is to simultaneously output acceptable figures for talks + ~Physical Review style figures. Because gnuplot is so efficient, it will happily push out a load of figures in under a second.

```
                    1 +----------------------------------------------------+
                      |=@%$ +     +     +     +    +     +     +     +     |
                  0.8 |-=@@%                                             +-|
                      |  = @B                                              |
                  0.6 |-+ = D$                            F              +-|
                      |    =A%B*              F           D                |
                  0.4 |-+   B&D%A#F           D           D     B        +-|
                      |      =F@D%D#          A           AB    D$   F   B |
                  0.2 |-+     B=A&F%         %@          #@DD   A%   D F D-|
                      |         B=BF$    B   @@    B DDA %@AA   @A  AABADA |
                      |            BB==F B$  =BAA  AAFFA@ABBB FBBBFFFBFBFFF|
                    0 |-+              BB%BBB@BBBBBBBBBBBBB BBBBBBBBBBBBBBB|
                      |                 D @A@$D#@@F@  A A    A D  D   @AAAD|
                 -0.2 |-+                 @@A   A%@A  B      D        @D F-|
                      |                   A$B   D$@@         F        A    |
                 -0.4 |-+                 D     F A%                  D  +-|
                      |                   B       D#                  B    |
                 -0.6 |-+                         B                      +-|
                      |     +     +     +     +   F+     +     +     +     |
                 -0.8 +----------------------------------------------------+
                      0     1     2     3     4    5     6     7     8     9
                                    Distance (lattice units)
```
It defaults to using the `dumb` terminal, so you can see what's going on in the shell. You set a `prefix` variable for the filename, `load gnuplot-render.gpt` and it will replot to PDF and PNG terminals. 
As every figure is always slightly unique, I now download a fresh copy of this to whichever REPO I am doing data analysis in, and then customise it further there.

## Gnuplot resources

A very useful resource for modern (less ugly) gnuplot is http://www.gnuplotting.org/ & associated Github repos https://github.com/Gnuplotting.

The best book resource is definitely https://www.manning.com/books/gnuplot-in-action-second-edition .

## Other Jarv Gnuplot bits

(This is mainly a reference for myself.)

### Phonons: 
Band structure: https://github.com/WMD-group/Phonons/blob/master/2016_MAPbX3-CompleteAssignment/Theory/band.gpt 
pDoS (decomposed + coloured): https://github.com/WMD-group/Phonons/blob/master/2016_MAPbX3-CompleteAssignment/Theory/phonon_pDoS_Eigenmodes.gpt

Phonon eigenmode energy decomposition: https://github.com/jarvist/Julia-Phonons/blob/master/plot-mode-decomposition/MAPI_mode.gpt

Crossing zero / autocorrelation function: https://github.com/jarvist/MAPI-MD-analysis/blob/master/timetocrosszero.gpt ; plot: https://github.com/jarvist/MAPI-MD-analysis/blob/master/300K_FAPI_correlation.png
