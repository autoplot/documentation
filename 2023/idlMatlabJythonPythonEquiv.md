What are the equivalents in Matlab, IDL, SciPy, and Autoplot Jython?

IDL: findgen
Matlab: 
SciPy: np.arange
Jython: findgen

IDL: fltarr(10)
Matlab: zeros(10)
SciPy: np.zeros(10)
Jython: zeros(10)

| IDL  | Matlab  | SciPy  | Jython  |
|---|---|---|---|
|  findgen(10) |   |  np.arange(10) | findgen(10)  |
|  fltarr(10) |   |  np.zeros(10) | zeros(10)  |
|  where(d>0) | find | np.where(d>0)  | where(d.gt(0) ) | 
