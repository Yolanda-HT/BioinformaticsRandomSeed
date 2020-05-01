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
 *Y<sub>ij</sub><sup>l</sup>* ≈ *&alpha;<sub>i</sub>Y<sub>ij</sub><sup>C</sup>* <br>
 *S<sub>ij</sub><sup>l</sup>* ≈ *&beta;<sub>i</sub>S<sub>ij</sub>*
 
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
 *Y<sub>ij</sub><sup>d</sup>* ≈ *Y<sub>ij</sub><sup>l</sup>* * *&theta;<sub>i</sub>* <br>
 *S<sub>ij</sub><sup>d</sup>* ≈ *S<sub>ij</sub><sup>l</sup>* * *&theta;<sub>i</sub>* <br>
 
| Variable | Symbol |
| --- | --- |
| Capture rate | *&theta;* |
| Endo cDNA | *Y<sup>d</sup>* |
| Spike in cDNA | *S<sup>d<sup>* |

3. **Relative abundance** <br>
cDNA:  *Y<sub>ij</sub><sup>d</sup>* / &Sigma;<sub>j=1</sub><sup>n<sup> (*Y<sub>ij</sub><sup>d</sup>* +  *S<sub>ij</sub><sup>d</sup>* ) <br>
Spike in:  *S<sub>ij</sub><sup>d</sup>* / &Sigma;<sub>j=1</sub><sup>n<sup> (*Y<sub>ij</sub><sup>d</sup>* +  *S<sub>ij</sub><sup>d</sup>* ) 

4. **Multinomial sampling of R reads**
*R<sub>i</sub>* = *&gamma;* &Sigma;<sub>j=1</sub><sup>n<sup> (*Y<sub>ij</sub><sup>d</sup>* +  *S<sub>ij</sub><sup>d</sup>*)
