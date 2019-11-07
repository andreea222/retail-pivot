# retail-pivot
retail = pd.read_excel('file.xlsx')
import pandas as pd
import numpy as np
table = pd.pivot_table(retail,
                      index = ['year','Category'],
                    columns= ['Chain'],
                      values=['Total Units','Total Sales'],
                      aggfunc= {'Total Units':len, 'Total Sales':[np.sum, np.mean]},
                     fill_value=0)
                    
table
