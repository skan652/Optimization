# 🎯 Optimization Project - M2 IASD

A comprehensive implementation of optimization algorithms in Python, covering matrix factorization and vehicle routing problems.

## 📋 Overview

This project implements and compares various optimization techniques, including gradient descent (GD) and stochastic gradient descent (SGD), applied to two main problem domains:

1. **Matrix Factorization** - Low-rank approximation with regularization
2. **Vehicle Routing Problem (VRP)** - Last-mile delivery route optimization

## 🚀 Features

### Project 2.2: Matrix Factorization

- **Q1**: Scalar linear regression with closed-form and gradient descent solutions
- **Q2**: Matrix-based gradient descent for higher-dimensional problems
- **Q3**: Rank-1 matrix factorization (GD vs SGD comparison)
- **Q4**: Rank-r factorization with multiple rank analysis
- **Q5**: Regularized factorization with λ parameter tuning

**Key Implementations:**

- Batch size analysis for SGD convergence
- Singular value decomposition (SVD) analysis
- Loss visualization and convergence tracking
- Regularization impact on model capacity

### Project 1: Vehicle Routing Problem

Real-world delivery optimization using the [Package Delivery Dataset](https://www.kaggle.com/datasets/rajashrideka/package-delivery-dataset) (Bangalore, India).

**Components:**

- Nearest neighbor TSP heuristic
- Capacity-constrained route splitting
- Distance matrix computation using Haversine formula
- Visual route mapping and cost analysis

**Dataset:** 100 real delivery locations with coordinates and demands from Kaggle

## 🔧 Setup on Kaggle

1. Open [Kaggle Notebooks](https://www.kaggle.com/code)
2. Create a new notebook or upload `SkanderAdamAfi_Projet_Optimization.ipynb`
3. Add the [Package Delivery Dataset](https://www.kaggle.com/datasets/rajashrideka/package-delivery-dataset) to your notebook
4. Click **"Run All"** - all required libraries are pre-installed!

**Execution notes:**

- All cells run sequentially from top to bottom
- Each section is self-contained with its own data generation
- Visualizations display inline automatically
- Total runtime: ~10-15 seconds

## 📊 Key Results

### Matrix Factorization

- **Convergence Analysis**: SGD shows faster initial convergence but higher variance
- **Batch Size Impact**: Optimal batch sizes balance speed and stability
- **Regularization**: λ controls effective rank and prevents overfitting

### Vehicle Routing

- **Route Optimization**: Efficiently clusters deliveries into capacity-constrained routes
- **Cost Minimization**: Minimizes total distance traveled from depot
- **Scalability**: Handles 100+ delivery locations

## 🔬 Algorithms Implemented

| Algorithm | Function | Application |
| --------- | -------- | ----------- |
| Gradient Descent | `gd_scalar()`, `gd_scalar_matrix()` | Linear regression |
| Stochastic GD | `sgd_rank_1()`, `sgd_rank_r()` | Matrix factorization |
| Regularized GD | `gd_rank_r_reg()`, `sgd_rank_r_reg()` | Regularized factorization |
| Nearest Neighbor | `nearest_neighbors()` | TSP heuristic |
| Route Splitting | `split_routes()` | VRP capacity constraints |

## 📈 Visualizations

The notebook includes comprehensive visualizations:

- **Convergence plots**: Loss vs iterations for GD/SGD comparison
- **Batch size analysis**: Impact of mini-batch sizes on convergence
- **Singular value plots**: Regularization effect on matrix spectrum
- **Route maps**: Geographic visualization of optimized delivery routes

## 📝 Implementation Details

### Matrix Factorization Implementation

- **Objective**: Minimize $\frac{1}{2}\|UV^T - X\|_F^2 + \frac{\lambda}{2}(\|U\|_F^2 + \|V\|_F^2)$
- **Gradient Computation**: Analytical gradients for U and V matrices
- **Convergence**: Frobenius norm loss tracking per iteration

### Vehicle Routing Implementation

- **Objective**: Minimize total route distance subject to capacity constraints
- **Method**: Greedy nearest neighbor with capacity-aware route splitting
- **Constraints**: Vehicle capacity = 5000 units, each package = 1 unit

## 📚 Dataset Attribution

**Package Delivery Dataset** by Rajashri Deka  
Source: [Kaggle](https://www.kaggle.com/datasets/rajashrideka/package-delivery-dataset)  
License: Community Data License Agreement

The dataset contains real delivery coordinates from Bangalore, India, including customer locations, distances, delivery fees, and package weights.

## 🎓 Educational Value

This project demonstrates:

- ✅ Numerical optimization fundamentals
- ✅ GD vs SGD trade-offs (speed vs stability)
- ✅ Hyperparameter tuning (learning rate, batch size, regularization)
- ✅ Real-world application to logistics optimization
- ✅ Clean code practices and documentation

## 🐛 Known Considerations

- **Q2**: Matrix GD convergence depends on initialization
- **Q3**: SGD variance increases with smaller batch sizes
- **Q5**: Optimal λ is problem-dependent (requires tuning)
- **VRP**: Greedy heuristic not guaranteed optimal (good approximation)

## 👤 Author

**Skander Adam Afi**  
M2 IASD - Optimization Project

## 📄 License

This project is part of academic coursework for educational purposes.

---

Last Updated: February 2026
