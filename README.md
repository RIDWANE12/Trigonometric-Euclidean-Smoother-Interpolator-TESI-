# Trigonometric-Euclidean-Smoother-Interpolator-TESI-
# Paper Title: Trigonometric-Euclidean-Smoother Interpolator (TESI) for continuous time-series and non-time-series data augmentation for deep neural network applications in agriculture
# Paper DOI: https://doi.org/10.1016/j.compag.2023.107646

# How to use TESI 
# Install the Package
pip install Syndenv

# Import the Package
import Syndenv
import pandas as pd
from Syndenv import Syndbox

# Load the Data
df=pd.read_excel('/content/file_name.xlsx')

# Apply the TESI ob the Input Dataframe
df1=Syndbox.TESI(df, Equation='Euc_Log', start=0.01, augmentation_factor=20)

# Apply the TESI to Extract the Output as Dataframe
df1.pd_frame(save=True)

# Apply the TESI to Extract the Output as numpy array 
df1= df.arr()

# Parameters

start: (float): default=0.01: The starting value of the angle sequence.

stop: (int): default=1: The end value of the angle's sines vector. Should be always 1 because the angle's max sine is 1.

augmentation_factor: (int): default (0.01): The number of times the data is augmented. Should be from 0 to infinity.

Equation: default='Euc_p1': Either the Euclidean or the following transformed Euclidean formulas.

'Euc_p1': The linear polynomial.

'Euc_p2': The quadratic polynomial.

'Euc_p3': The cubic polynomial.

'Euc_Log': The log-transformed euclidian formula.
