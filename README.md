# Proyecto-Servicios-Interconnect
Pronosticar los clientes que tienen probabilidad de irse para ofrecer códigos promocionales.

## Descripción del proyecto

Al operador de telecomunicaciones Interconnect le gustaría poder pronosticar su tasa de cancelación de clientes. Si se descubre que un usuario o usuaria planea irse, se le ofrecerán códigos promocionales y opciones de planes especiales. El equipo de marketing de Interconnect ha recopilado algunos de los datos personales de sus clientes, incluyendo información sobre sus planes y contratos.

**Servicios de Interconnect**

Interconnect proporciona principalmente dos tipos de servicios:
1.	Comunicación por teléfono fijo. El teléfono se puede conectar a varias líneas de manera simultánea.
2.	Internet. La red se puede configurar a través de una línea telefónica (DSL, línea de abonado digital) o a través de un cable de fibra óptica.

Algunos otros servicios que ofrece la empresa incluyen:

- Seguridad en Internet: software antivirus (ProtecciónDeDispositivo) y un bloqueador de sitios web maliciosos (SeguridadEnLínea).
- Una línea de soporte técnico (SoporteTécnico).
- Almacenamiento de archivos en la nube y backup de datos (BackupOnline).
- Streaming de TV (StreamingTV) y directorio de películas (StreamingPelículas)

La clientela puede elegir entre un pago mensual o firmar un contrato de 1 o 2 años. Puede utilizar varios métodos de pago y recibir una factura electrónica después de una transacción.

**Objetivo**: Pronosticar los clientes que tienen probabilidad de irse para ofrecer códigos promocionales.

Para cumplir el objetivo, vamos a seguir estos pasos:

- Carga de los datos: cargar los 4 archivos csv para la manipulaciónde estos.

- EDA: Cambio de formato a las columnas por ejemplo: formato de fecha, flotante, object, etc. Vamos a unir todos los dataframes en uno solo para determinar los clientes que tiene cada uno de los diferentes servicios. Después vamos dividir dicha base en dos los activos y los dados de baja. Trabajaremos con ambas secciones para encontrar patrones, ver la proporción de las categorías y ver si hay alguna con mayor peso que otra y por último ver si hay colinealidad o correlaciones para determinar que variables podemos eliminar y tener menos ruido en los modelos.
Dada las columnas de cada dataframe podemos crear algunas hipótesis con respecto a cuáles tendrán mayor relevancia como parte del entrenamiento de los modelos estas son: 
    - Type: que es la periodicidad del pago
    - PaymentMethod: método de pago
    - SeniorCitizen: Si es mayor de 60 años
    - MultipleLines: Si cuenta con una línea telefónica o varias.
    - InternetService: por que medio se le brinda el servicio de internet

    Durante el proceso de EDA veremos si fueron correctas estás hipótesis o no. Tambén vamos a estandarizar, realizar One-Hot y dividir la base en 75 y 25 para la parte de entrenamiento y validación. Para la obtención de los mejores hiperparámetros vamos a usar GridSearchCV por ello solo vamos a dividir en dos la base.
    
- Creación de modelos:

    - Arbol de decisión
    - Bosque aleatorio
    - Regresión logística
    - Boosting
    - Red neuronal
- Determinar que modelo tuvo mejor resultado bajo las métricas; AUC-ROC, exactitud.
- Conclusiones
