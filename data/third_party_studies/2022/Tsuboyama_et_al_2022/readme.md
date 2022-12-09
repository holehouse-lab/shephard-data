# About
These data are take from *Tsuboyama et al. 2022*, with the notebook in `parse_K50_dG_Dataset1_Dataset2.ipynb` providing code to extract out new [SHEPHARD tracks file](https://shephard.readthedocs.io/en/latest/shephard_file_types.html#track-files).

The data here are large-scale mutagenesis data, whereby for many of the proteins we have deep saturation mutagenesis (i.e. each residue mutated to every other residue). To keep things simple, the SHEPHARD files reflect data from constructs where a single point mutation was made and a deltaG is assigned based on that mutation.

[SHEPHARD track files](https://shephard.readthedocs.io/en/latest/shephard_file_types.html#track-files) contain at least 3 columns:

* Column 1: protein identifier
* Column 2: track name
* Column 3 onwards: per-amino acid scores 

For the SHEPHARD files here, the track names are written as `deltaG_<X>` where `<X>` is an amino acid. The deltaGs are then the values where the residue at each position is mutated to amino acid `<X>`.

For example, if your had a sequence that was:

    >my_protein
    MAPL...
    
You might have a corresponding deltaG file with the format:

    my_protein    deltaG_A    2.3    0    5.6    1.2    ... 

i.e. for `my_protein` the ΔG reported based on the combined digestion by tyrpsin and chymotrypsin for the M1A mutation is 2.3 kcal/mol, whereas for P3A the ΔG is 5.6 kcal/mol.


### Refs
Tsuboyama, K., Dauparas, J., Chen, J., Mangan, N. M., Ovchinnikov, S., & Rocklin, G. J. (2022). Mega-scale experimental analysis of protein folding stability in biology and protein design. In bioRxiv (p. 2022.12.06.519132). https://doi.org/10.1101/2022.12.06.519132

