# Mechanistic Model of rAAV Production

This repository contains a Python implementation of a mechanistic model for recombinant adeno-associated virus (rAAV) production via triple transfection of HEK293 cells, as described in:

Nguyen, T. N. T., et al. (2021). *Mechanistic model for production of recombinant adeno-associated virus via triple transfection of HEK293 cells.* Molecular Therapy: Methods & Clinical Development, 21, 642-655.

The model simulates the key intracellular biological processes, from delivery of three distinct plasmids into the cell nucleus to assembly and release of functional viral capsids.

## About the Model

The simulation is based on a system of 15 ordinary differential equations (ODEs) describing the concentration changes of relevant molecular species over time. It has two main components:

- **Plasmid Delivery**: Trafficking of helper, packaging, and vector plasmids from the extracellular space into the cell nucleus.  
- **Viral Vector Synthesis**: Synthesis of Rep and Capsid proteins, replication of viral DNA, assembly of empty capsids, and packaging of DNA into full virions.

The model allows exploration of process parameters, such as the initial plasmid ratio, to predict their impact on final virion yield.

## Repository Contents

- `raav_production_model.py`: Main Python script with the ODE model, simulation functions, and plotting logic.  
- `requirements.txt`: Python dependencies required to run the simulation.  
- `README.md`: Documentation file.

## Getting Started

### Prerequisites

- Python 3.7 or higher

### Installation

Clone the repository:
```bash
git clone https://github.com/iamabhinav13/Mechanistic-Model-of-rAAV-Production.git
cd Mechanistic-Model-of-rAAV-Production
```
Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```
Install required packages:
```bash
pip install -r requirements.txt
```
Running the Simulation
Run the main script:

```bash
python raav_production_model.py
```

## Simulations Included

- **Baseline Simulation**: Production dynamics with a 1:1:1 plasmid ratio.  
- **Plasmid Ratio Comparison**: Compares full virion yields across different plasmid ratios to demonstrate model predictions.

## Expected Output

Running the script generates four plots:

- **Viral DNA Replication and Packaging (Baseline)**: Copies of viral DNA and full virions over time.  
- **Total Capsid and Full Virion Production (Baseline)**: Total capsids (empty + full) vs full virions on a log scale.  
- **Impact of Plasmid Ratio on Production (Time-series)**: Full virion production curves for different plasmid ratios.  
- **Normalized Full Virion Yield (Bar Chart)**: Final yields at 60 hours for different ratios, replicating the paper’s validation analysis.
