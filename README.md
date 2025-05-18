# Neural-Network_Sudoku-solver
This project explores the application of deep neural networks to classification problems, with a particular focus on how different model architectures, optimization strategies, and regularization techniques impact performance. It represents my latest and most refined attempt at solving Sudoku puzzles using neural networks.

In this implementation, each Sudoku grid is represented as a flattened vector of 81 input features. For each puzzle, 10 to 20 values are randomly masked and treated as the target labels y—this number can be adjusted during preprocessing. The model is trained to accurately impute these missing values.

A central element of this approach is the use of masking and a custom training loop, which accommodates variable numbers of target labels per sample. To efficiently handle the large dataset, a chunked processing strategy is used during training for memory efficiency and scalability.

In the next phase of this project, I plan to alter the underlying data through a mapping transformation that intentionally breaks some of the fundamental rules of Sudoku (e.g., the constant sum of rows, columns, or boxes). While these logical constraints are no longer directly valid in the transformed data, the original Sudoku structure can still be reconstructed. The goal is to evaluate whether the neural network can still learn and generalize the underlying rules of Sudoku despite such transformations, and how these data changes influence preprocessing requirements and architectural adjustments needed to sustain model performance.


Note: for the Dataset you can use any flattened complete Sudoku dataset. having 81 features for each puzzle. name x0 ,...,x80
