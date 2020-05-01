# Single-cell mRNA quantification and differential analysis with Census
> Last update: 05/01/2020 <br>
> By: Huitian (Yolanda) Diao

# Information 
| ~ | Description |
| --- | --- |
| Objective | Convert TPM to relative transcript counts without need spike-in standards or UMIs for differential analysis |
| Environment | R |
| Dependency | Monocole2 |
| Development release | [Github](https://github.com/cole-trapnell-lab/monocle-release) |

# Algorithm
1. **Cell lysate recovery** <br>
  - *Y<sub>ij</sub><sup>l</sup>* ≈ *&alpha;<sub>i</sub>Y<sub>ij</sub><sup>C</sup>* <br>
  - *S<sub>ij</sub><sup>l</sup>* ≈ *&beta;<sub>i</sub>S<sub>ij</sub>*
 
| Variable | Symbol |
| --- | --- |
| Gene | *j* |
| Cell | *i* |
| Recovery rate of RNA |  *&alpha;* |
| Recovery rate of spike-in | *&beta;* |
| Total RNA | *Y<sup>C</sup>* |
| Total Spike in | *S* |
| Lysate RNA | *Y<sup>l</sup>* |
| Lysate Spike in | *S<sup>l</sup>* |

2. **cDNA conversion** <br>
  - *Y<sub>ij</sub><sup>d</sup>* ≈ *Y<sub>ij</sub><sup>l</sup>* * *&theta;<sub>i</sub>* <br>
  - *S<sub>ij</sub><sup>d</sup>* ≈ *S<sub>ij</sub><sup>l</sup>* * *&theta;<sub>i</sub>* <br>
 
| Variable | Symbol |
| --- | --- |
| Capture rate | *&theta;* |
| Endo cDNA | *Y<sup>d</sup>* |
| Spike in cDNA | *S<sup>d<sup>* |

3. **Relative abundance** <br>
 - cDNA:  *Y<sub>ij</sub><sup>d</sup>* / &Sigma;<sub>j=1</sub><sup>n</sup> (*Y<sub>ij</sub><sup>d</sup>* +  *S<sub>ij</sub><sup>d</sup>* )
 - Spike in:  *S<sub>ij</sub><sup>d</sup>* / &Sigma;<sub>j=1</sub><sup>n</sup> (*Y<sub>ij</sub><sup>d</sup>* +  *S<sub>ij</sub><sup>d</sup>* ) 

4. **Multinomial sampling of R reads**
*R<sub>i</sub>* = *&gamma;* &Sigma;<sub>j=1</sub><sup>n</sup> (*Y<sub>ij</sub><sup>d</sup>* +  *S<sub>ij</sub><sup>d</sup>*)

| Variable | Symbol |
| --- | --- |
| Average reads per cDNA | *&gamma;* &Sigma |

5. **Read count**
  - cDNA: *Y<sub>ij</sub><sup>r</sup>* ~ multinomial (Relative cDNA abundance, Multinomial sampling of cDNA)
  - Spike in: *Y<sub>ij</sub><sup>r</sup>* ~ multinomial (Relative spike in abundance, Multinomial sampling of spike in)

6. **Simulator for sc-RNA-seq process**

7. **Estimate capture rate based on spike-in**
Probability to observe at least one copy of transcript: *&rho;* = 1 - (1 - *&theta;*)<sup>S</sup>

| Variable | Symbol |
| --- | --- |
| Copy number | S |

...

Use a assumed value of *&theta;* to convert TPM *X<sub>ij</sub><sup>l</sup>*  to real transcript number (*Y<sub>ij</sub><sup>l</sup>* ) with a Gaussian kernel density estimation to identify peak of distribution (with capturing probability distribution from 7.)


