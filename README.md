# Ejercicio de Pruebas Unitarias en Java

Este proyecto es un ejemplo de pruebas unitarias en Java utilizando JUnit y Mockito.

## 📌 Requisitos

- Java 11 o superior
- Apache Maven
- IntelliJ IDEA



## 🧪 Ejecución de pruebas

```sh
mvn test
```


## 📦 Dependencias

El proyecto utiliza las siguientes dependencias:

```xml
<dependencies>
    <dependency>
        <groupId>junit</groupId>
        <artifactId>junit</artifactId>
        <version>4.13.2</version>
        <scope>test</scope>
    </dependency>
    <dependency>
        <groupId>org.mockito</groupId>
        <artifactId>mockito-core</artifactId>
        <version>4.8.0</version>
        <scope>test</scope>
    </dependency>
</dependencies>
```

## ✨ Ejemplo de Código

### Implementación de `ServicioA`

```java
public interface ServicioA {
    int sumar(int a, int b);
}
```

### Implementación de `ServicioAImpl`

```java
public class ServicioAImpl implements ServicioA {
    @Override
    public int sumar(int a, int b) {
        return a + b;
    }
}
```

### Prueba Unitaria con JUnit

```java
import org.junit.Test;
import static org.junit.Assert.assertEquals;

public class TestServicioA {
    @Test
    public void testSumar() {
        ServicioA servicioA = new ServicioAImpl();
        assertEquals(4, servicioA.sumar(2, 2));
    }
}
```


