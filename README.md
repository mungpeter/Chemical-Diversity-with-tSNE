# Chemical-Diversity-with-tSNE
Using t-SNE to visualize the diversity of chemical libraries

- Based on this PCA/TSNE analysis
https://github.com/rdkit/rdkit-tutorials/blob/master/notebooks/005_Chemical_space_analysis_and_visualization.ipynb

- 2024.01.05, 2024.01.18
Peter M.U. Ung @ gRED

- Degrader_CRBN.murcko_cluster.full_space.ipynb
Analysis the chemical diversity and overlaps of multiple libraries. Using the generic/hetero Murcko structures
to group similar cpds together instead of using full-mol structure, which is sensitive to the decorations and
affect the proper grouping of cpds with the same scaffold. PCA does an okay job in spreading out the chemical 
space but still very packed. Use t-SNE to better spread out the chemical space for visualization.

- Degrader_CRBN.glutarimide.RGroup_space.ipynb
Analysis the chemical diversity and overlaps of multiple libraries' glutarimide analogs. Specifically the lactam
and phthalimide core analogs. Do R-Group decomposition to extract the exit vectors R1-R4 on the core phenyl ring.
Phthalimide core has internal symmetry so might need to rearrange R1-->R4 or R2-->R3 vectors, since R3/R4 are 
biologically more relevant. Since many cpds has [H] substituent as exit vector, need to remove them to better 
analyze the true chemical space. Use t-SNE to better spread out the chemical space for visualization. 

![Degrader_CRBN all_lib hetero_murcko_tSNE](https://github.com/mungpeter/Chemical-Diversity-with-tSNE/assets/52801335/a53c442f-f117-4a60-995a-945494c111b4)

- Python 3.9
  pandas 1.4.3
  rdkit 2022.09
  numpy 1.23.1
  seaborn 0.11.2
  sklearn 1.1.1
