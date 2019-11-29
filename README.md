# <center>Useful material for projects</center>
*This page is used to record the useful links, commands and references that I found can be very useful for doing projects.*

## Links
* Plotting with PLT: https://heasarc.gsfc.nasa.gov/docs/xte/recipes/plotting.html
* RA DEC flexible converter: http://www.astrouw.edu.pl/~jskowron/ra-dec/
* X-ray transition energies: https://www.nist.gov/pml/x-ray-transition-energies-database
* X-ray spectral fitting methods workshop: [here](https://www.mpe.mpg.de/resources/HE/Buchner/xrayworkshop/?fbclid=IwAR3aKISdmmASKO-IeX3skdzgFREszKa16WFbACG_tj-FQnHqeY0GYkFHyGs)
* MJD converter: http://www.csgnetwork.com/julianmodifdateconv.html


## References

## Commands
* To visualize the light curve
<pre><code>lcurve nser=1 cfile1=rate.fits window="-" dtnb=50 nbint=3000 outfile="lc" plot=yes plotdev="/xs"}
</pre></code>

* To group data with <code>grppha</code>
<pre><code>grppha source_spectrum.fits pn_25.grp comm= "chkey RESPFILE pn.rmf & chkey ANCRFILE pn.arf & chkey BACKFILE back_spectrum.fits & group min 25 & exit"
</pre></code>

* To download data with FTP from nasa's archive
<pre><code>wget -q -nH --no-check-certificate --cut-dirs=3 -r -l0 -c -N -np -R 'index*' -erobots=off --retr-symlinks https://heasarc.gsfc.nasa.gov/FTP/caldb/data/suzaku/
</pre></code>
