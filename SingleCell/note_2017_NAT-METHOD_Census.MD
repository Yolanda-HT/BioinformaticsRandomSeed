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
1. Cell lysate recovery:
 *Y<sub>ij</sub><sup>l</sup>* ≈ *&alpha;<sub>i</sub>Y<sub>ij</sub><sup>C</sup>*
 *S<sub>ij</sub><sup>l</sup>* ≈ *&beta;<sub>i</sub>S<sub>ij</sub>*
 
| Variable | Symbol |
| --- | --- |
| Recovery rate of RNA |  *α* |
| Recovery rate of spike-in | *β* |
| Total RNA | *Y<sup>C</sup>* |
| Total Spike in | *S* |
| Lysate RNA | *Y<sup>l</sup>* |
| Lysate Spike in | *S<sup>l</sup>* |

 h<sub>&theta;</sub>(x) = &theta;<sub>o</sub> x + &theta;<sub>1</sub>x
