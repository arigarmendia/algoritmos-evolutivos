# Optimización de curva de temperatura con algoritmos genéticos

Proyecto de optimización que utiliza Algoritmos Genéticos (GA) con codificación decimal para ajustar un polinomio cúbico a datos de temperatura a lo largo del día.

## Descripción del Problema

Dado un conjunto de 4 puntos de datos `(hora, temperatura)`, el objetivo es encontrar los coeficientes óptimos de un polinomio cúbico que mejor se ajuste a estos puntos:

```
y = a·x³ + b·x² + c·x + d
```

Donde:
- `x` = hora del día
- `y` = temperatura
- `a, b, c, d` = coeficientes a optimizar

### Representación
- **Tipo de cromosoma**: Decimal/Continuo
- **Genes**: 4 valores flotantes `[a, b, c, d]`

### Operadores Genéticos
- **Selección**: Torneo (tamaño 3)
- **Cruza**: Blend Crossover (`cxBlend`, alpha=0.5)
- **Mutación**: Gaussiana (`mutGaussian`, mu=0, sigma=3.0, indpb=0.2)

### Hiperparámetros
El proyecto evalúa 5 configuraciones diferentes.