# web-testing
Набор инструментов для тестирования вашего приложения на Java Spring Boot.

## Часть №1

Spring Boot Actuator - предоставляет REST-эндпоинты для мониторинга здоровья, метрик и производительности приложения.
```xml
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-actuator</artifactId>
        </dependency>
```

включим необходиме эндпоинты в application.properties
```properties
management.endpoints.web.exposure.include=health,info,env,beans,metrics
```

теперь при запуске нашего приложения мы можем смтореть различные метрики:
</br>
http://localhost:8080/actuator/helth - общее состояние приложения
</br>
http://localhost:8080/actuator/metrics/system.cpu.usage - загрузка процессора
</br>
http://localhost:8080/actuator/heapdump - скачать дамп памяти JVM в формате .hprof
</br>
и т.д.

## Часть №2

