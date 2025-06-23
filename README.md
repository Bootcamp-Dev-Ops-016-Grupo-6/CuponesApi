# Pruebas de Regresión Automatizadas en una API de Cupones

## Grupo 6

### Preguntas finales

1. ¿Por qué fue difícil detectar la regresión sin pruebas?

Porque sin realizar una prueba, no se muestra directamente que haya un error incluso aunque falte el cupón de BIENVENIDA, por lo que puede pasar fácilmente desapercibido sin realizar pruebas.

2. ¿Cómo te ayuda el testing automatizado a mantener calidad?

El testing automatizado se asegura de realizar pruebas cada vez que el código cambia, asegurándonos que cualquier cambio no vaya a romper el código que ya tenemos y detectando errores de forma temprana.

3. ¿Qué otras partes del código deberías cubrir con pruebas?

Utilizando Test Coverage, se descubrió que también se deberían agregar pruebas para algunas líneas faltantes en cupones.py, teniendo una cobertura del 88%. También deberían cubrirse las funciones críticas como entradas de usuario inválidas.

4. ¿Cómo evitarías errores similares en el futuro?

Haciendo uso de estrategias para mejorar la eficiencia en la ejecución de pruebas, tales como dividir las pruebas por tipo, hacer revisiones de código y exigir cobertura de pruebas antes de hacer merge a la rama main.

### Capturas de pantalla

- Test Failed
![Test Failed](app/assets/images/Test_fallido.png)


- Test Passed
![Test Passed](app/assets/images/Test_pasado.png)

5.  Resumen de cómo se detecto la regresión y cómo se evitarán en el futuro.

Gracias a una prueba unitaria que detectó que se había borrado el cupón BIENVENIDA, lo que rompió la lógica de los descuentos. Para evitar problemas similares a futuro, se usarán herramientas de cobertura de pruebas que detecten cambios inesperados y regresiones, además de automatizar las pruebas usando GitHub Actions para que se ejecuten en cada Commit.