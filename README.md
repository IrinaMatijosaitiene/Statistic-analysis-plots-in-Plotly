# Statistic-analysis-plots-in-Plotly
Box plot, histogram, and scatter plot
#import modules
import numpy as np
import pandas as pd
import scipy
import plotly
import plotly.plotly as py
import plotly.figure_factory as ff
plotly.tools.set_credentials_file(username='irimati', api_key='bRYNEEDEg7K2SJ3hLdzn')
plotly.tools.set_config_file(world_readable=True, sharing='public')

#import data
data = pd.read_csv('customers.csv')
customers = data[0:]

table = ff.create_table(customers)
#create a table in plotly
py.plot(table, filename='customers', sharing='public')
