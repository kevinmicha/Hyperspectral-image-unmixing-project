# Hyperspectral image unmixing project
Solving an unmixing problem using parallel computing techniques in Julia.

### Authors: Martina BALBI and Kevin MICHALEWICZ

A blind source separation problem whose goals are to:
<ul>
  <li>Extract the signatures of the pure materials (endmembers) present in the image</li>
  <li>Estimate their relative proportions (fractional abundances) in each pixel</li>
</ul>

The constraints are the following:
<ul>
  <li>Abundance non-negativity constraint (ANC)</li>
  <li>Abundance sum-to-one constraint (ASC)</li>
</ul>

This problem can be considered as **embarrassingly parallel** as it possesses several independent tasks that can be carried out before aggregating the results. Thus, the idea is to implement a projected gradient descent algorithm coded by us in a standard serial way and then using parallelization. After that, we perform a similar analysis using Julia libraries. 
