Primero es necesario entrar a la página oficial de Google Colab a través de:  
https://colab.research.google.com/  
E iniciar sesión con tu cuenta de Google.

### 1. Subir el archivo que dejamos en este repositorio a Colab

#### 1.1. En Colab selecciona:

• Archivo →Subir notebook

#### 1.2. Busca el archivo del proyecto con extensión .ipynb.

#### 1.3. Espera a que cargue.

Cuando termine, aparecerán varias celdas con código.

### 2. Subir la base de datos a Google Drive

Para que nuestro código que se subió en la parte 1 pueda leer el archivo Excel, primero se debe subir a Drive

#### 2.1. Abrimos Drive desde el link:

https://drive.google.com/drive/home

#### 2.2. Dar clic en:

• Nuevo → Subir archivo

#### 2.3. Selecciona la base de datos descargada aquí en el repositorio “Base”

#### 2.4. Y esperar a que se termine de subir.

### 3. Ya dentro del . ipynb que subimos, hay que darle permiso al notebook para leer archivos de Drive.

#### 3.1. Ejecutamos la línea de código con el botón que aparece a la izquierda.

```python
from google.colab import drive
drive.mount('/content/drive')
```

#### 3.2. Se abrirá un enlace.

#### 3.3. Da permisos a Google Colab.

### 4. Obtener la ruta del archivo.

#### 4.1. En el menú izquierdo de Colab abre la carpeta.

#### 4.2. Entra a:

• Drive → MyDrive

#### 4.3. Busca el archivo Excel que subiste.

#### 4.4. Da clic derecho sobre el archivo.

#### 4.5. Selecciona:

• Copiar ruta

### 5. Pegar la ruta en el código

#### 5.1. Busca en el notebook la línea

```python
base = pd.read_excel("")
base.head()
```

#### 5.2. Dentro de las comillas (“”) pega tu ruta de acceso

### 6. Instalar librerías necesarias

#### 6.1. Busca la celda

```python
# Tratamiento dedatos
import pandas as pd
import numpy as np

#Graficos
import matplotlib.pyplot as plt
from matplotlib import style
import seaborn as sns

#Procesado y modelado
from scipy.stats import pearsonr
from sklearn.linear_model import LinearRegression
from sklearn.model_selection import train_test_split
from sklearn.metrics import r2_score
from sklearn.metrics import mean_squared_error
import statsmodels.api as sm
import statsmodels.formula.api as smf
from scipy import stats
import statsmodels as sms

#from sklearn.datasets import load_boston
#from sklearn.datasets import fetch_california_housing
#from sklearn.datasets import fetch_openml

from statsmodels.stats.outliers_influence import variance_inflation_factor # para calcular el VIF

# configuración de matplotlib
plt.rcParams['image.cmap']="bwr"
plt.rcParams['figure.dpi']="100"
plt.rcParams['savefig.bbox']="tight"

style.use('ggplot') or plt.style.use('ggplot')

# configuración de warnings
import warnings
warnings.filterwarnings('ignore')

from matplotlib.pyplot import subplots
from statsmodels.api import OLS
import sklearn.model_selection as skm
import sklearn.linear_model as skl
from sklearn.preprocessing import StandardScaler
from ISLP import load_data
from ISLP.models import ModelSpec as MS
from functools import partial
from sklearn.pipeline import Pipeline
from sklearn.decomposition import PCA
from sklearn.cross_decomposition import PLSRegression

from ISLP.models import \
(Stepwise ,
sklearn_selected ,
sklearn_selection_path)

from l0bnb import fit_path
```

#### 6.2. Solo hace falta ejecutarla Ctrl + Enter

### 7. Ejecutar todas las celdas

#### 7.1. en orden de arriba hacia abajo se ejecuta celda por celda
