# PaSR_UDF
In the scope of my masther thesis on supersonic combustion, the PaSR UDF is implemented. During this study different cases are analysed as the 2D and 3D cases of a scramjet and this UDF has been modified. The files uploaded here are thus similar but may contain minor changes.

This code has only been modified but the original one has been previously used by Ferrarotti et al. 2018 PROCI. 

For the thesis, only the static and dynamic approaches have been used. Different trials have been made to obtain better results.
The chemical time scale is computed taking the maximum from the formation rate. A change which was implemented, to see if it suits better, is to take the minimum from the formation rates, in our case this was less advantageous so it is brought back to the maximum one. 

The mixing time scale is either taken based on the integral time scale or the Kolmogorov one. One can also implement different formulations as the geometric mean of the integral and the Kolmogorov time scales. This was done during the thesis. 

The instructions to use the dynamic PaSR model are written in the code and have to be followed carefully to have proper results.

Finally, the last thing that have been changed, in the 3D case of DLR, is the gamma formulation. Indeed, the gamma was going too quickly from 0 to 1 and vice-versa leading to no reaction so in order to smooth this transition, an exponent has been introduced. Then, several exponents are tried, after an apriori study to see which one suits the best. 

For the sake of simplicity, the last version of the code contains a UDM10 which is for the Damkhöler number.
