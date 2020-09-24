# Diploma
Algorithm for prediction of protein complex structure based on structural patterns
To do: automate the PATH choice.
I didn’t figure out how to make the selection automated (I found the KEGG library in python, but I didn’t understand how to extract proteins from a Uniprot out of the PATH). 
I went to a random path, looked for the ‘Uniprot’ tab. 
I downloaded the .html file with the Uniprot proteins, looked (automated) whether the protein was reviewed or not  the protein, and loaded the .pdb if its 3D structure was known. 

Pyhton scripts:
1) KEGG_get_protein_pdb_from_pathway — processing KEGG path's .html file,
2) concatenate_templates — creating a file with templates for which both the interface and the complete structures are known
3) kegg_i и kegg_fs — target's 'run' for interface and full structures libraries, 
4) clean_top_from_not_common — cleaning tops from unnecessary templates,
5) one_top — creation of a single top,
6) sort_one_top — sorting the top (tm-align >= 0.4),
7) matrix_complex_pymol — creating the final top (applying transformation matrix + rmsd <=10.0)
