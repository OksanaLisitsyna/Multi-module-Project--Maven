## Multi-module-Project--Maven
В этом задании отрабатывался навык сборки проектов с помощью фреймворка для автоматизации сборки **Maven**.
</br></br>
 В проекте три модуля с разделением по функциональности:
* db - модуль работы с базой данных;
* api - модуль работы с web;
* service - слой сервисов.
</br></br>

Для решения задачи в каждой директории создаем **pom.xml**,
где обязательно указываем *parent* - в качестве родительского модуля с его данными и название *artifactId* текущего модуля:
```
 <parent>
        <artifactId>App</artifactId>
        <groupId>ru.netology</groupId>
        <version>1.0-SNAPSHOT</version>
    </parent>
    <modelVersion>4.0.0</modelVersion>
    <artifactId>db</artifactId>
    <packaging>jar</packaging>
 ```
 </br>
 
 Чтобы подключить новые модули к проекту, добавляем в корне проекта в файл **pom.xml** новые созданные модули:
```
<modules>
    <module>db</module>
    <module>api</module>
    <module>service</module>
  </modules> 
  ```
