# gnuplot-snippets
Snippets for rendering ~publication quality figures in GNUPLOT.

## Why gnuplot in 2018?

I know, I know. All the cool kids use Matplotlib. Gnuplot is old, cranky, and ugly by default. The thing is, I was a cool kid once. 

I've wrestled repeatedly with Matplotlib magics to make a publication quality figure; I've returned to ~6 month old scripts to find them rendering very differently; sometimes the low performance is an actual problem. So I have returned to gnuplot as my main plotter.

In this repository I will try and collate / collect my useful bits and bobs for plotting with gnuplot, starting with my 'gnuplot-render.gpt' function for outputting acceptable figures for talks + ~Physical Review style figures.

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
