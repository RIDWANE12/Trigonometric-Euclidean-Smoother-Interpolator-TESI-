# Trigonometric-Euclidean-Smoother-Interpolator-TESI-
Trigonometric-Euclidean-Smoother Interpolator (TESI) for continuous time-series and non-time-series data augmentation for deep neural network applications in agriculture


pip install Syndenv

import Syndenv
import pandas as pd
from Syndenv import Syndbox

df=pd.read_excel('/content/file_name.xlsx')
df1=Syndbox.TESI(df, Equation='Euc_Log', start=0.01, augmentation_factor=20)

df1.pd_frame(save=True)

# or;
df1.arr()
