# Quantum Control with Neural Networks: PINN and QubiNN

This repository contains the Jupyter notebooks, training data, and saved models used in the project **"Quantum Control with Neural Networks: PINN and QubiNN"**, which explores the application of neural networks for single-qubit quantum control tasks.

## Project Overview

The project investigates two neural network architectures:
- **Physics-Informed Neural Networks (PINNs):** Incorporates the Schrödinger equation to enforce physical consistency in predicting control fields and expectation values.
- **QubiNN:** A purely data-driven feedforward neural network used as a baseline for comparison.

Both models were trained and benchmarked using data generated via QuTiP simulations. The results highlight the trade-offs between accuracy, physical consistency, and computational efficiency.

---

## Repository Structure

### Folders
- **`notebooks/`**: Contains the main Jupyter notebooks used in the project:
  - `training_data.ipynb`: Generates training data using QuTiP simulations.
  - `QuPINN.ipynb`: Implements and trains the PINN for predicting control fields and expectation values.
  - `QubiNN.ipynb`: Implements and trains the QubiNN for comparison.
  - `benchmarking.ipynb`: Benchmarks the performance of PINN and QubiNN against QuTiP simulations.
  
- **`data/`**: Contains the training data used for the models, including:
  - `training_data.csv`: The dataset of control fields and expectation values generated from QuTiP simulations.

- **`models/`**: Contains the saved model weights for PINN and QubiNN:
  - `QuPINN_model.pth`
  - `QubiNN_model.pth`

### Additional Files
- **`README.md`**: This documentation file.
- **`requirements.txt`**: A list of dependencies needed to run the notebooks.

---

## How to Use

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/quantum-control-neural-networks.git
cd quantum-control-neural-networks
```

### 2. Set Up the Environment
Create and activate a Python virtual environment, then install the required dependencies:
```bash
pip install -r requirements.txt
```

### 3. Run the Notebooks
Navigate to the `notebooks/` folder and open the desired notebook using Jupyter Notebook or JupyterLab:

```bash
jupyter notebook notebooks/training_data.ipynb
```

---

## Key Features

1. **Training Data Generation**:
   - The `training_data.ipynb` notebook uses QuTiP to generate control fields and expectation values for diverse target states on the Bloch sphere.
2. **Model Training**:
   - The `QuPINN.ipynb` and `QubiNN.ipynb` notebooks train the respective models on the generated data.
3. **Benchmarking**:
   - The `benchmarking.ipynb` notebook evaluates the models on test target states, comparing their performance against QuTiP simulations in terms of accuracy, fidelity, and computational efficiency.

---

## Results Summary

- **Performance**:
  - QubiNN excels in predicting expectation values and achieves higher computational efficiency.
  - PINN slightly outperforms in control field predictions but is more computationally intensive.
- **Speedup**:
  - Both models achieve significant speedup compared to QuTiP simulations, with QubiNN achieving up to ~5000x faster predictions.

For detailed results and visualizations, refer to the `benchmarking.ipynb` notebook.

---

## Dependencies

The project requires the following Python libraries:
- `numpy`
- `matplotlib`
- `torch`
- `qutip`
- `pandas`
- `scikit-learn`

These can be installed using the `requirements.txt` file.

---

## License

This repository is licensed under the MIT License. See the `LICENSE` file for more details.

---

## Contact

For questions, suggestions, or collaboration inquiries, feel free to contact:
- **Name**: Diego Alducin
- **Email**: diego.alducin@gmail.com
- **GitHub**: [datdiego](https://github.com/datdiego)
