
# Planeacion estudiante A

## Cálculos de vuelo

### Funciones una sola expresión

***Función calcularDistanciaTotal*** *función de una sola expresión*

Datos entrada: un parámetro normal
Resultado: Regresa el cálculo de distancia total ida y vuelta
```
fun calcularDistanciaTotal(distanciaIda:Double):Double=distanciaIda*2
```
**Caso 1:**  calcularDistanciaTotal(5) -> resultado=10  
**Caso 2:** calcularDistanciaTotal(7.5)-> resultado=15

***Función calcularTiempoBase*** *función de una sola expresión*

Datos entrada: un parámetro normal
Resultado: Regresa el cálculo de distancia total ida y vuelta
```
fun calcularTiempoBase(distanciaTotal:Double):Double=distanciaTotal/2
```
**Caso 1:**  calcularTiempoBase(10) -> resultado=5  
**Caso 2:** calcularTiempoBase(15)-> resultado=7.5

### Lamdas en variables

***Lamda aumentar 20%*** 

Datos entrada: un parámetro tiempo
Resultado: Regresa el tiempo aumentado el 20%
```
val aumentarVeintePorciente: (Double) -> Double ={valor->valor*1.20}
```
**Caso 1:**    
**Caso 2:** 

***Lamda disminuir 10%***
Datos entrada: un parámetro tiempo
Resultado: Regresa el tiempo disminuido un 10%  

```
val disminuirDiezPorciento: (Double) -> Double ={valor->valor*0.90}
```  
**Caso 1:**    
**Caso 2:**

### Función de orden superior
***Función para aplicar ajuste de tiempo***
Datos entrada: un párametro tiempo, una función
Resultado: Regresa el tiempo ajustado

```
fun aplicarAjuste(valorBase: Double,ajuste: (Double) -> Double): Double{
      ajuste(valorBase)
}
```

**Caso 1:**    val tiempoConLluvia=aplicarAjuste(15, aumentarVeintePorciento)
**Caso 2:**    val tiempoEmergencia=aplicarAjuste(10,disminuirDiezPorciento)

***Función para selección del ajuste***
Datos entrada: un párametro tiempo base tipo double, un parámetro condicion String,  
               una función ajusteLluvia, función ajusteEmergencias
Resultado: Regresa el tiempo ajustado

```
fun calcularTiempoFinal(tiempoBase: Double,condicion: String, ajusteLluvia:(Double)->Double),
                       ajusteEmergenica: (Double) -> Double):Double{
     when (condicion){
        "normal": return tiempoBase
        "lluvia": return ajusteLluvia(tiempoBase)
        "emergencia": return ajusteEmergencia(tiempoBase)
     }
}
```

**Caso 1:**    
**Caso 2:**   