import altair as alt
import pandas as pd
#read the file
file = r'Clastic_TS_Altair4.xlsx'
df = pd.read_excel(file,index_col=False)

alt.Chart(source).mark_circle(size=400).encode(
   x='POROSITY:Q',
   y='LPerm:Q',
   color = alt.Color('LPerm:Q', scale=alt.
                     Scale(scheme = 'rainbow')),
   tooltip=['image'], # Must be a list for the image to render
).properties(
   width=700,
   height=700,
   title='Porosity vs. Permeability Cross Plot: hover over Sample to see Thin Section',
