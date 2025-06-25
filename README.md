# Simulaciones de Electrónica de Potencia

**Autor:** Juan Felipe Martínez
**Repositorio:** simulaciones-electronica-potencia

---

## Índice

* [Descripción](#descripción)
* [Objetivos](#objetivos)
* [Estructura del Repositorio](#estructura-del-repositorio)
* [Requisitos](#requisitos)
* [Instalación](#instalación)
* [Simulaciones Incluidas](#simulaciones-incluidas)
* [Uso](#uso)
* [Resultados y Análisis](#resultados-y-análisis)
* [Buenas Prácticas](#buenas-prácticas)
* [Contribuciones](#contribuciones)
* [Licencia](#licencia)
* [Referencias](#referencias)

---

## Descripción

Este repositorio contiene un conjunto de simulaciones de electrónica de potencia realizadas con distintas herramientas (MATLAB/Simulink, Python y LTspice). El propósito es analizar el comportamiento dinámico y estático de convertidores estáticos (rectificadores, inversores, DC-DC) bajo diferentes condiciones de carga y estrategias de control.

## Objetivos

1. Implementar modelos detallados de convertidores de potencia.
2. Validar respuestas transitoria y en estado estacionario.
3. Comparar diferentes técnicas de modulación PWM.
4. Evaluar el perfil de armónicos y la eficiencia de los sistemas.

## Estructura del Repositorio

```
simulaciones-electronica-potencia/
├── README.md                 # Documentación general
├── requirements.txt          # Dependencias Python
├── simulations/
│   ├── rectificador_controlado/    # Código y modelos de rectificador controlado
│   ├── inversor_tripolar/          # Modelos y scripts de inversor trifásico
│   ├── convertidor_dc_dc/          # Buck, boost y buck-boost
│   └── analisis_armonicos/         # Jupyter notebooks de FFT y espectros
├── datasheets/                   # Hojas de datos de componentes usados
├── results/
│   ├── figuras/                  # Gráficos generados (PNG, PDF)
│   └── tablas/                   # Resultados numéricos (CSV)
└── docs/
    └── informe_final.pdf        # Informe completo con conclusiones
```

## Requisitos

* Python ≥ 3.8
* MATLAB/Simulink R2019b o superior
* LTspice XVII
* Bibliotecas Python:

  * NumPy
  * SciPy
  * matplotlib
  * pandas
  * jupyter

Instalación de dependencias Python:

```bash
pip install -r requirements.txt
```

## Instalación

1. Clonar el repositorio:

   ```bash
   ```

git clone [https://github.com/tu-usuario/simulaciones-electronica-potencia.git](https://github.com/tu-usuario/simulaciones-electronica-potencia.git)
cd simulaciones-electronica-potencia

````

2. Descargar e instalar las herramientas de simulación si aún no están disponibles.
3. Configurar rutas en los scripts de Python o en MATLAB si es necesario.

## Simulaciones Incluidas

- **Rectificador Controlado**: Análisis de puente de diodos con control de ángulo de disparo.
- **Inversor Trifásico**: Generación de onda seno modulada por PWM y control vectorial.
- **Convertidores DC-DC**: Topologías buck, boost y buck-boost, respuesta al escalón de carga.
- **Análisis de Armónicos**: Transformada rápida de Fourier para señales de salida.

## Uso

### MATLAB/Simulink

1. Abrir el modelo `.slx` en la carpeta correspondiente.
2. Ajustar parámetros (frecuencia de conmutación, voltajes, cargas).
3. Ejecutar la simulación.
4. Guardar datos de salida usando `To Workspace`.

### Python

Ejemplo para analizar respuesta temporal del buck converter:

```bash
python simulations/convertidor_dc_dc/buck_response.py --Vin 48 --Vout 12 --Rload 10
````

### LTspice

1. Abrir el archivo `.asc`.
2. Correr la simulación transitoria o de AC.
3. Graficar resultados en la interfaz.

## Resultados y Análisis

* Los gráficos generados se encuentran en `results/figuras/`.
* Las tablas con valores de THD y eficiencia en `results/tablas/`.
* En `docs/informe_final.pdf` se presentan conclusiones detalladas.

## Buenas Prácticas

* Versionar código y modelos con Git.
* Documentar cada script y modelo.
* Mantener separadas las dependencias de cada entorno.

## Contribuciones

Las contribuciones son bienvenidas:

1. Hacer un fork del proyecto.
2. Crear una rama con tu feature: `git checkout -b feature/nombre-feature`.
3. Hacer commit de tus cambios: `git commit -m "Agrega nueva simulación"`.
4. Push a tu rama: `git push origin feature/nombre-feature`.
5. Abrir un Pull Request.

## Licencia

Este proyecto está bajo la licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.

## Referencias

1. Rashid, M. H. **"Power Electronics: Circuits, Devices, and Applications"**, Prentice Hall.
2. Mohan, N., Undeland, T., Robbins, W. **"Power Electronics: Converters, Applications and Design"**.
3. Documentación oficial de MATLAB/Simulink.
