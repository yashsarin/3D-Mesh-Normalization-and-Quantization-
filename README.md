Mesh Normalization, Quantization & Error Analysis
Author: Yash Sarin
Date: 2025-11-07 19:47

Project Overview:
This assignment focuses on mesh preprocessing — normalization, quantization,
and reconstruction error analysis. The goal was to standardize mesh coordinates,
compress data efficiently, and measure reconstruction accuracy.

How to Run:
1. Install dependencies:
   pip install trimesh open3d numpy matplotlib
2. Open Mesh_Assignment.ipynb in Jupyter.
3. Place your mesh files (.obj) or zip in 'input_meshes/'.
4. Run all cells to generate processed meshes and error plots.

Summary of Results:
 - branch.obj: MSE(MinMax)=7.82e-07, MSE(UnitSphere)=2.34e-06
 - cylinder.obj: MSE(MinMax)=7.97e-07, MSE(UnitSphere)=2.57e-06
 - explosive.obj: MSE(MinMax)=1.24e-07, MSE(UnitSphere)=3.90e-07
 - fence.obj: MSE(MinMax)=1.57e-07, MSE(UnitSphere)=3.61e-07
 - girl.obj: MSE(MinMax)=2.05e-07, MSE(UnitSphere)=3.52e-07
 - person.obj: MSE(MinMax)=7.89e-07, MSE(UnitSphere)=1.76e-06
 - table.obj: MSE(MinMax)=1.49e-07, MSE(UnitSphere)=4.70e-07
 - talwar.obj: MSE(MinMax)=1.31e-07, MSE(UnitSphere)=5.85e-07


Observations:
• Both normalization methods preserve geometry well (MSE < 1e-6).
• Min–Max normalization maintains proportions better for varied meshes.
• Unit Sphere normalization ensures scale invariance.
• Quantization with 1024 bins yields minimal reconstruction loss.

Folder Structure:
- input_meshes/        → input .obj or .zip files
- output_meshes/       → reconstructed meshes (.ply)
- plots/               → per-axis MSE plots
- summary.json         → aggregated error metrics
- README.txt           → project overview
- Report.pdf           → final report
