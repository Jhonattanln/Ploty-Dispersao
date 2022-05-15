## Criando gráfico de dispersão com Plotly

#### Tratando dados da série histórica de preços




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>RRRP3</th>
      <th>ALPA4</th>
      <th>ABEV3</th>
      <th>AMER3</th>
      <th>ASAI3</th>
      <th>AZUL4</th>
      <th>B3SA3</th>
      <th>BIDI11</th>
      <th>BPAN4</th>
      <th>BBSE3</th>
      <th>...</th>
      <th>VIVT3</th>
      <th>TIMS3</th>
      <th>TOTS3</th>
      <th>UGPA3</th>
      <th>USIM5</th>
      <th>VALE3</th>
      <th>VIIA3</th>
      <th>VBBR3</th>
      <th>WEGE3</th>
      <th>YDUQ3</th>
    </tr>
    <tr>
      <th>Data</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2017-01-25</th>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>...</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
    </tr>
    <tr>
      <th>2017-01-26</th>
      <td>-</td>
      <td>7.954093</td>
      <td>14.884808</td>
      <td>12.208539</td>
      <td>-</td>
      <td>-</td>
      <td>5.059228</td>
      <td>-</td>
      <td>1.412158</td>
      <td>19.227179</td>
      <td>...</td>
      <td>25.117261</td>
      <td>7.846246</td>
      <td>8.708409</td>
      <td>29.749848</td>
      <td>4.514089</td>
      <td>24.579933</td>
      <td>3.154388</td>
      <td>-</td>
      <td>5.764304</td>
      <td>14.246222</td>
    </tr>
    <tr>
      <th>2017-01-27</th>
      <td>-</td>
      <td>7.797252</td>
      <td>14.893407</td>
      <td>11.958403</td>
      <td>-</td>
      <td>-</td>
      <td>5.07858</td>
      <td>-</td>
      <td>1.520093</td>
      <td>19.615813</td>
      <td>...</td>
      <td>25.602256</td>
      <td>7.794227</td>
      <td>8.628952</td>
      <td>29.630619</td>
      <td>4.648437</td>
      <td>24.653088</td>
      <td>3.204142</td>
      <td>-</td>
      <td>5.778625</td>
      <td>14.542112</td>
    </tr>
    <tr>
      <th>2017-01-30</th>
      <td>-</td>
      <td>7.767377</td>
      <td>14.592443</td>
      <td>11.631303</td>
      <td>-</td>
      <td>-</td>
      <td>5.028817</td>
      <td>-</td>
      <td>1.448136</td>
      <td>19.29536</td>
      <td>...</td>
      <td>25.48613</td>
      <td>7.681518</td>
      <td>8.355623</td>
      <td>29.034474</td>
      <td>4.505132</td>
      <td>23.592347</td>
      <td>3.184241</td>
      <td>-</td>
      <td>5.7285</td>
      <td>14.27233</td>
    </tr>
    <tr>
      <th>2017-01-31</th>
      <td>-</td>
      <td>7.759908</td>
      <td>14.790219</td>
      <td>11.544718</td>
      <td>-</td>
      <td>-</td>
      <td>5.111755</td>
      <td>-</td>
      <td>1.439142</td>
      <td>19.029452</td>
      <td>...</td>
      <td>26.087251</td>
      <td>7.759547</td>
      <td>8.292058</td>
      <td>29.215525</td>
      <td>4.702176</td>
      <td>23.541138</td>
      <td>3.233994</td>
      <td>-</td>
      <td>5.696278</td>
      <td>13.837198</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 92 columns</p>
</div>






    RRRP3    1007
    ALPA4      70
    ABEV3      70
    AMER3      70
    ASAI3    1077
             ... 
    VALE3      70
    VIIA3      71
    VBBR3     289
    WEGE3      70
    YDUQ3      70
    Length: 92, dtype: int64






    IGTI11    232
    ASAI3      50
    CMIN3      43
    LREN3      14
    PETR3      14
    PCAR3      14
    MULT3      14
    MRVE3      14
    BEEF3      14
    CASH3      14
    MRFG3      14
    MGLU3      14
    LWSA3      14
    PRIO3      14
    LCAM3      14
    RENT3      14
    KLBN11     14
    JHSF3      14
    JBSS3      14
    ITUB4      14
    dtype: int64






<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>RRRP3</th>
      <th>ALPA4</th>
      <th>ABEV3</th>
      <th>AMER3</th>
      <th>AZUL4</th>
      <th>B3SA3</th>
      <th>BIDI11</th>
      <th>BPAN4</th>
      <th>BBSE3</th>
      <th>BRML3</th>
      <th>...</th>
      <th>VIVT3</th>
      <th>TIMS3</th>
      <th>TOTS3</th>
      <th>UGPA3</th>
      <th>USIM5</th>
      <th>VALE3</th>
      <th>VIIA3</th>
      <th>VBBR3</th>
      <th>WEGE3</th>
      <th>YDUQ3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>246.000000</td>
      <td>246.000000</td>
      <td>246.000000</td>
      <td>246.000000</td>
      <td>246.000000</td>
      <td>246.000000</td>
      <td>246.000000</td>
      <td>246.000000</td>
      <td>246.000000</td>
      <td>246.000000</td>
      <td>...</td>
      <td>246.000000</td>
      <td>246.000000</td>
      <td>246.000000</td>
      <td>246.000000</td>
      <td>246.000000</td>
      <td>246.000000</td>
      <td>246.000000</td>
      <td>246.000000</td>
      <td>246.000000</td>
      <td>246.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>0.000177</td>
      <td>-0.000118</td>
      <td>0.000334</td>
      <td>-0.002819</td>
      <td>-0.001219</td>
      <td>-0.001925</td>
      <td>0.000793</td>
      <td>0.001571</td>
      <td>-0.001136</td>
      <td>-0.000302</td>
      <td>...</td>
      <td>0.000597</td>
      <td>-0.000097</td>
      <td>0.000460</td>
      <td>-0.001546</td>
      <td>0.000873</td>
      <td>0.000255</td>
      <td>-0.003945</td>
      <td>0.000524</td>
      <td>-0.000217</td>
      <td>-0.001550</td>
    </tr>
    <tr>
      <th>std</th>
      <td>0.032124</td>
      <td>0.026090</td>
      <td>0.018834</td>
      <td>0.037494</td>
      <td>0.033473</td>
      <td>0.023174</td>
      <td>0.051023</td>
      <td>0.043847</td>
      <td>0.014963</td>
      <td>0.022650</td>
      <td>...</td>
      <td>0.013676</td>
      <td>0.016862</td>
      <td>0.024251</td>
      <td>0.026832</td>
      <td>0.031427</td>
      <td>0.022163</td>
      <td>0.035175</td>
      <td>0.022500</td>
      <td>0.021904</td>
      <td>0.029403</td>
    </tr>
    <tr>
      <th>min</th>
      <td>-0.073618</td>
      <td>-0.105580</td>
      <td>-0.057010</td>
      <td>-0.107584</td>
      <td>-0.141805</td>
      <td>-0.083799</td>
      <td>-0.141142</td>
      <td>-0.121753</td>
      <td>-0.045148</td>
      <td>-0.066587</td>
      <td>...</td>
      <td>-0.032825</td>
      <td>-0.037951</td>
      <td>-0.062854</td>
      <td>-0.123343</td>
      <td>-0.075366</td>
      <td>-0.075913</td>
      <td>-0.124823</td>
      <td>-0.072178</td>
      <td>-0.083045</td>
      <td>-0.082875</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>-0.020228</td>
      <td>-0.013308</td>
      <td>-0.010673</td>
      <td>-0.025685</td>
      <td>-0.018664</td>
      <td>-0.015368</td>
      <td>-0.028345</td>
      <td>-0.025910</td>
      <td>-0.012179</td>
      <td>-0.014058</td>
      <td>...</td>
      <td>-0.007148</td>
      <td>-0.010074</td>
      <td>-0.014742</td>
      <td>-0.015724</td>
      <td>-0.018128</td>
      <td>-0.014705</td>
      <td>-0.023904</td>
      <td>-0.014892</td>
      <td>-0.011834</td>
      <td>-0.016927</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>-0.001554</td>
      <td>-0.000509</td>
      <td>0.000000</td>
      <td>-0.006202</td>
      <td>-0.002837</td>
      <td>-0.002168</td>
      <td>-0.001074</td>
      <td>-0.001757</td>
      <td>-0.000659</td>
      <td>-0.001859</td>
      <td>...</td>
      <td>0.000231</td>
      <td>-0.000846</td>
      <td>-0.001448</td>
      <td>-0.002282</td>
      <td>0.000255</td>
      <td>-0.000526</td>
      <td>-0.003702</td>
      <td>0.000440</td>
      <td>-0.002583</td>
      <td>-0.002624</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>0.017312</td>
      <td>0.012109</td>
      <td>0.009962</td>
      <td>0.018603</td>
      <td>0.017020</td>
      <td>0.013129</td>
      <td>0.023054</td>
      <td>0.025865</td>
      <td>0.008207</td>
      <td>0.015054</td>
      <td>...</td>
      <td>0.007408</td>
      <td>0.009224</td>
      <td>0.015797</td>
      <td>0.014592</td>
      <td>0.015544</td>
      <td>0.012498</td>
      <td>0.014722</td>
      <td>0.012627</td>
      <td>0.010799</td>
      <td>0.011713</td>
    </tr>
    <tr>
      <th>max</th>
      <td>0.122239</td>
      <td>0.166537</td>
      <td>0.097240</td>
      <td>0.096939</td>
      <td>0.113068</td>
      <td>0.059357</td>
      <td>0.248337</td>
      <td>0.153122</td>
      <td>0.035533</td>
      <td>0.070922</td>
      <td>...</td>
      <td>0.068118</td>
      <td>0.083770</td>
      <td>0.077682</td>
      <td>0.095140</td>
      <td>0.095299</td>
      <td>0.070181</td>
      <td>0.112801</td>
      <td>0.095694</td>
      <td>0.081710</td>
      <td>0.098157</td>
    </tr>
  </tbody>
</table>
<p>8 rows × 89 columns</p>
</div>



#### Calculando a volatilidade

#### Criando gráficos interativos






<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>RRRP3</th>
      <th>ALPA4</th>
      <th>ABEV3</th>
      <th>AMER3</th>
      <th>AZUL4</th>
      <th>B3SA3</th>
      <th>BIDI11</th>
      <th>BPAN4</th>
      <th>BBSE3</th>
      <th>BRML3</th>
      <th>...</th>
      <th>VIVT3</th>
      <th>TIMS3</th>
      <th>TOTS3</th>
      <th>UGPA3</th>
      <th>USIM5</th>
      <th>VALE3</th>
      <th>VIIA3</th>
      <th>VBBR3</th>
      <th>WEGE3</th>
      <th>YDUQ3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>...</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
      <td>226.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>49.838086</td>
      <td>39.683647</td>
      <td>29.255032</td>
      <td>57.374161</td>
      <td>50.847251</td>
      <td>36.475153</td>
      <td>75.150301</td>
      <td>68.207659</td>
      <td>23.451290</td>
      <td>34.526612</td>
      <td>...</td>
      <td>21.299246</td>
      <td>26.408779</td>
      <td>37.932285</td>
      <td>42.281627</td>
      <td>48.068535</td>
      <td>34.105134</td>
      <td>53.059889</td>
      <td>35.091808</td>
      <td>33.025782</td>
      <td>45.537419</td>
    </tr>
    <tr>
      <th>std</th>
      <td>12.251310</td>
      <td>12.702410</td>
      <td>6.958674</td>
      <td>14.958493</td>
      <td>15.834410</td>
      <td>9.434829</td>
      <td>26.485561</td>
      <td>12.919250</td>
      <td>4.094815</td>
      <td>8.193909</td>
      <td>...</td>
      <td>5.956192</td>
      <td>6.319966</td>
      <td>7.042736</td>
      <td>10.788186</td>
      <td>13.452130</td>
      <td>6.816976</td>
      <td>18.434895</td>
      <td>9.212504</td>
      <td>6.540775</td>
      <td>11.843149</td>
    </tr>
    <tr>
      <th>min</th>
      <td>25.081900</td>
      <td>19.759784</td>
      <td>10.816742</td>
      <td>31.928400</td>
      <td>26.145955</td>
      <td>18.976552</td>
      <td>37.645013</td>
      <td>43.692537</td>
      <td>15.954763</td>
      <td>22.451909</td>
      <td>...</td>
      <td>11.035702</td>
      <td>13.570076</td>
      <td>22.867031</td>
      <td>21.355091</td>
      <td>22.180677</td>
      <td>17.427091</td>
      <td>22.556708</td>
      <td>21.395539</td>
      <td>20.377454</td>
      <td>22.084865</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>38.891003</td>
      <td>31.529512</td>
      <td>24.651137</td>
      <td>47.274023</td>
      <td>36.815654</td>
      <td>29.497882</td>
      <td>53.353883</td>
      <td>57.315822</td>
      <td>20.533519</td>
      <td>27.625323</td>
      <td>...</td>
      <td>16.433909</td>
      <td>22.316900</td>
      <td>31.423059</td>
      <td>34.768165</td>
      <td>36.461444</td>
      <td>30.166857</td>
      <td>36.754208</td>
      <td>28.483406</td>
      <td>28.928792</td>
      <td>36.374233</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>50.630872</td>
      <td>35.351585</td>
      <td>30.542699</td>
      <td>55.073738</td>
      <td>48.950968</td>
      <td>35.394832</td>
      <td>67.213511</td>
      <td>68.014592</td>
      <td>23.104309</td>
      <td>33.133084</td>
      <td>...</td>
      <td>21.306338</td>
      <td>25.890570</td>
      <td>38.222162</td>
      <td>40.742204</td>
      <td>49.602698</td>
      <td>33.704010</td>
      <td>52.610951</td>
      <td>31.633197</td>
      <td>31.839916</td>
      <td>48.400899</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>58.449833</td>
      <td>51.744040</td>
      <td>34.326673</td>
      <td>69.256636</td>
      <td>61.999183</td>
      <td>43.286211</td>
      <td>100.437467</td>
      <td>76.867129</td>
      <td>25.611401</td>
      <td>39.133120</td>
      <td>...</td>
      <td>25.075968</td>
      <td>29.334387</td>
      <td>43.921633</td>
      <td>52.168569</td>
      <td>57.313339</td>
      <td>37.449721</td>
      <td>65.916906</td>
      <td>41.510032</td>
      <td>35.672880</td>
      <td>54.003184</td>
    </tr>
    <tr>
      <th>max</th>
      <td>74.737969</td>
      <td>61.971713</td>
      <td>40.052078</td>
      <td>93.547872</td>
      <td>85.661607</td>
      <td>59.378252</td>
      <td>136.790769</td>
      <td>104.783657</td>
      <td>34.055664</td>
      <td>54.471470</td>
      <td>...</td>
      <td>37.207698</td>
      <td>43.532868</td>
      <td>51.490485</td>
      <td>64.527068</td>
      <td>74.645337</td>
      <td>53.460362</td>
      <td>91.408098</td>
      <td>57.128474</td>
      <td>53.286600</td>
      <td>70.006237</td>
    </tr>
  </tbody>
</table>
<p>8 rows × 89 columns</p>
</div>



#### Calculando rentabilidade




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Retorno</th>
    </tr>
    <tr>
      <th>Ativo</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>RRRP3</th>
      <td>-10.747539</td>
    </tr>
    <tr>
      <th>ALPA4</th>
      <td>-10.564936</td>
    </tr>
    <tr>
      <th>ABEV3</th>
      <td>1.822570</td>
    </tr>
    <tr>
      <th>AMER3</th>
      <td>-57.034014</td>
    </tr>
    <tr>
      <th>AZUL4</th>
      <td>-36.230366</td>
    </tr>
  </tbody>
</table>
</div>






<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>Nome</th>
      <th>Classe</th>
      <th>Bolsa / Fonte</th>
      <th>Tipo de Ativo</th>
      <th>Ativo /\nCancelado</th>
      <th>Participação\nno Ibovespa\n\nem %</th>
      <th>Segmento listagem\nBovespa</th>
      <th>Subsetor Bovespa</th>
      <th>Data da\nÚlt Cotação</th>
      <th>...</th>
      <th>ROE\n12 meses\n\nem %</th>
      <th>ROA\n12 meses\n\nem %</th>
      <th>Lucro Líquido\n12 meses\n\nem %</th>
      <th>Lucro p/ Ação\n12 meses\n\nem R$</th>
      <th>Valor Patrimonial\np/ Ação\n\nem R$</th>
      <th>Margem Bruta\n12 meses\n\nem %</th>
      <th>Margem Líquida\n12 meses\n\nem %</th>
      <th>EBITDA\n12 meses\n\nem milhares</th>
      <th>Margem EBITDA\n12 meses\n\nem %</th>
      <th>Capex vs\nDepreciação\n12 meses\nem %</th>
    </tr>
    <tr>
      <th>Código</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>VALE3</th>
      <td>1</td>
      <td>Vale</td>
      <td>ON</td>
      <td>Bovespa</td>
      <td>Ação</td>
      <td>ativo</td>
      <td>15.410</td>
      <td>Novo Mercado</td>
      <td>Mineração</td>
      <td>2022-01-25</td>
      <td>...</td>
      <td>50.913922</td>
      <td>20.083844</td>
      <td>95687024</td>
      <td>18.739226</td>
      <td>37.060195</td>
      <td>61.204143</td>
      <td>31.391452</td>
      <td>135567300</td>
      <td>44.83832</td>
      <td>219.182501</td>
    </tr>
    <tr>
      <th>PETR4</th>
      <td>2</td>
      <td>Petrobras</td>
      <td>PN</td>
      <td>Bovespa</td>
      <td>Ação</td>
      <td>ativo</td>
      <td>7.185</td>
      <td>Nível 2</td>
      <td>Petróleo gás e biocombustíveis</td>
      <td>2022-01-25</td>
      <td>...</td>
      <td>43.444773</td>
      <td>13.95245</td>
      <td>135054000</td>
      <td>10.353566</td>
      <td>28.294335</td>
      <td>51.073834</td>
      <td>34.564239</td>
      <td>279473000</td>
      <td>71.031389</td>
      <td>20.757951</td>
    </tr>
    <tr>
      <th>ITUB4</th>
      <td>3</td>
      <td>ItauUnibanco</td>
      <td>PN</td>
      <td>Bovespa</td>
      <td>Ação</td>
      <td>ativo</td>
      <td>5.497</td>
      <td>Nível 1</td>
      <td>Intermediários financeiros</td>
      <td>2022-01-25</td>
      <td>...</td>
      <td>18.101326</td>
      <td>1.228607</td>
      <td>26346000</td>
      <td>2.22333</td>
      <td>11.749069</td>
      <td>42.256953</td>
      <td>20.412963</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
    </tr>
    <tr>
      <th>BBDC4</th>
      <td>4</td>
      <td>Bradesco</td>
      <td>PN</td>
      <td>Bovespa</td>
      <td>Ação</td>
      <td>ativo</td>
      <td>4.956</td>
      <td>Nível 1</td>
      <td>Intermediários financeiros</td>
      <td>2022-01-25</td>
      <td>...</td>
      <td>17.071557</td>
      <td>1.466455</td>
      <td>24239402</td>
      <td>2.494621</td>
      <td>15.233548</td>
      <td>57.317059</td>
      <td>21.936403</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
    </tr>
    <tr>
      <th>PETR3</th>
      <td>5</td>
      <td>Petrobras</td>
      <td>ON</td>
      <td>Bovespa</td>
      <td>Ação</td>
      <td>ativo</td>
      <td>4.616</td>
      <td>Nível 2</td>
      <td>Petróleo gás e biocombustíveis</td>
      <td>2022-01-25</td>
      <td>...</td>
      <td>43.444773</td>
      <td>13.95245</td>
      <td>135054000</td>
      <td>10.353566</td>
      <td>28.294335</td>
      <td>51.073834</td>
      <td>34.564239</td>
      <td>279473000</td>
      <td>71.031389</td>
      <td>20.757951</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 69 columns</p>
</div>






<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Ativo</th>
      <th>Volatilidade</th>
      <th>Participação no Ibovespa</th>
      <th>Retorno</th>
      <th>Subsetor Bovespa</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>84</th>
      <td>VALE3</td>
      <td>35.111145</td>
      <td>15.410</td>
      <td>-1.396955</td>
      <td>Mineração</td>
    </tr>
    <tr>
      <th>65</th>
      <td>PETR4</td>
      <td>44.410944</td>
      <td>7.185</td>
      <td>16.516591</td>
      <td>Petróleo gás e biocombustíveis</td>
    </tr>
    <tr>
      <th>49</th>
      <td>ITUB4</td>
      <td>30.043458</td>
      <td>5.497</td>
      <td>-14.334771</td>
      <td>Intermediários financeiros</td>
    </tr>
    <tr>
      <th>11</th>
      <td>BBDC4</td>
      <td>31.934553</td>
      <td>4.956</td>
      <td>-15.957502</td>
      <td>Intermediários financeiros</td>
    </tr>
    <tr>
      <th>64</th>
      <td>PETR3</td>
      <td>43.386394</td>
      <td>4.616</td>
      <td>23.726372</td>
      <td>Petróleo gás e biocombustíveis</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>60</th>
      <td>BEEF3</td>
      <td>41.031497</td>
      <td>0.118</td>
      <td>19.151749</td>
      <td>Alimentos processados</td>
    </tr>
    <tr>
      <th>37</th>
      <td>EZTC3</td>
      <td>47.556512</td>
      <td>0.100</td>
      <td>-49.096347</td>
      <td>Construção civil</td>
    </tr>
    <tr>
      <th>51</th>
      <td>JHSF3</td>
      <td>41.640478</td>
      <td>0.085</td>
      <td>-19.361889</td>
      <td>Construção civil</td>
    </tr>
    <tr>
      <th>59</th>
      <td>CASH3</td>
      <td>99.488813</td>
      <td>0.072</td>
      <td>11.146717</td>
      <td>Programas e serviços</td>
    </tr>
    <tr>
      <th>68</th>
      <td>POSI3</td>
      <td>71.975608</td>
      <td>0.033</td>
      <td>130.825465</td>
      <td>Computadores e equipamentos</td>
    </tr>
  </tbody>
</table>
<p>89 rows × 5 columns</p>
</div>



#### Criando gráfico de disperção



#### Criando gráfico de Box






