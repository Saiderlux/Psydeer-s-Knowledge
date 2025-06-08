Funciones de agregación: Suma, promedio, conteo de información, mínimo , máximo.

```MySQL
SELECT departamento, SUM(salario) AS total_salario
FROM empleados
WHERE salario > 40000
GROUP BY departamento
```

```MySQL
SELECT departamento, COUNT(*) AS total_salario
FROM empleados
WHERE salario > 40000
GROUP BY departamento
```