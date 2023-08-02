# Desafio-FieldPRO
Repositório com a solução do desafio FieldPRO. Nele, é necessário construir um modelo de calibração de um sensor de
chuva baseado em impactos mecânicos a partir dos dados de dois datasets, onde o arquivo Sensor_FieldPRO.csv mostra os impactos mecânicos que o sensor sofreu a cada hora e o Estacao_Convencional.csv mostra o valor do sensor.

### Tratamento de valores NaN
O tratamento de valores NaN foi realizado obtendo-se a média entre os valores da linhas anterior e posterior à que possui este valor. Supondo que não houveram variações bruscas dos impactos em uma hora, é possível solucionar este problema desta maneira.

### Detecção de outliers
A detecção de outliers é realizada a partir da biblioteca PyOD, que marca como '1' as amostras que correspondem a outliers e '0' as que não. Dessa forma, podemos excuí-los.

### Calibração
A calibração é um modelo de regressão linear criado a partir da biblioteca Scikit-Learn.
