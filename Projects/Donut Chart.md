```python
import pandas as pd
import matplotlib.pyplot as plt

def donut(values, labels, title):
    fig, ax = plt.subplots(figsize=(2.4,2.4))
    wedges, _ = ax.pie(values, wedgeprops={'width': 0.4})
    ax.set_title(title)
    plt.legend(labels,bbox_to_anchor=(0, 1), loc='upper right', ncol=1)
    plt.show()

df = pd.read_csv('studies_published.csv')
donut(df['k'], df['study_design'], 'Types of Studies Published')


```