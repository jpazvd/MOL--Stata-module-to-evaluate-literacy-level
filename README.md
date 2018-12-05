# MOL: Stata module to evaluate literacy level

## Description

A country's overall level of literacy is usually measured by taking the number of adults who are
literate as a percentage of the total number of adults - the so-called literacy rate. Following Sen
(1985) there has been increased use of the literacy rate and other social indicators to evaluate the
overall standard of living in a country.

mol implements an alternative aproaches to evaluate the aggregate literacy level in a country or
region or any type of group. The resulting 'effective literacy' proposed by Basu and Foster (1998).
This measure takes into account the intrahousehold externality arising from the presence of a
literate member in the household. The extensions proposed by Subramanian (2004) are also
implemented.

### Option

by(housevar) indicates the variable that will be used to identify the members of a given household.

by(groupvar) repeats the command for each group of observations for which the values of the
    variables in varlist are the same. Groupvar must be an integer variable.

alpha(number) specifies the sensitivity alpha used. Alpha is contained within the interval [0,1]. If
    alpha is omited, only the houseshould effective literacy is calculated.  Multiple alphas are
    allowed to be calculated at once.

rank returns the rank of different groups according to each indicator.

gen generates tree new variables in the dataset with the output of the exercise.

format(%fmt) specifies the format to be used to display the estimated inequality indices. The
    default is to use a %6.5f format.

### Output Variables

     R:	'Crude' Literacy Rate .
     Re:	Effective Literacy [alpha = household literacy rate].
     (1-I):	Isolated Rate of Literacy (1-I).
     I:	Isolated Rate of Illiteracy (1-I).
     Q:	Efficiency Loss. Q is contained within the interval [0,1]: Q= 0 when I = 0, 
	and Q= 1 when I=1-R (which, of course, is the maximum value I can attain, 
	corresponding to a situation in which all illiterates are isolated illiterates).
     R*:Externality-adjusted Literacy Rate (Subramanian, 2004).


## Suggested Citation
[Joao Pedro Azevedo, 2008. "MOL: Stata module to evaluate literacy level," Statistical Software Components S456987, Boston College Department of Economics.](https://ideas.repec.org/c/boc/bocode/s456987.html)

## Reference

Basu, Kaushik and Foster, James E. (1998) On measuring literacy. Economic Journal, vol.108, no.451, Nov., pp.1733-1749.

Sen, A. (1985), Commodities and Capability. Amsterdam: North-Holland.

Subramanian, S (2004) Measuring literacy: some extensions of the Basu-Foster framework. Journal of Development Economics, vol.73, pp453-463.

#### Handle: RePEc:boc:bocode:s456987 

#### Note: This module should be installed from within Stata by typing "ssc install mol". Windows users should not attempt to download these files with a web browser.

#### Keywords
literacy; effective literacy