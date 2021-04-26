# JS_project2
Простой JS проект с readme.md

## Второй заголовок
...
###### Шестой заголовок

Одна простая строка
Текст на следующей строке

Первая строка<br/>
Вторая строка с разрывом строки

Третья строка с нового абзаца с *курсивом*, **жирным**, ***жирным курсивом***, ~~зачеркнутым~~ шрифтом.
>Цитата

---
Ссылка на [github](https://github.com/NikolasT1503/JS_project2)

Другой тип ссылки - [изучаем markdown][1]

![plantUML](./img/uml.png)


### Выделение кода

```javascript
function someFunction() {
    return 2*2
}

somefunction()
```
### Пример UML в виде диаграммы

```PlantUML
@startuml packaging
component "Create-project-app" as project  {

    folder "/node_modues" {
        artifact "/..." as node_modules
    }
    folder "/src" {
        artifact "/..." as src
    }
    folder "/public/..." as public {
        file "/index.html" as public_index
        file "/favicon.ico" as public_favicon
        file "/manifest.json" as public_manifest
    }
}

cloud {
    card "localhost:3000" {
        file "manifest.json" as manifest
        file "main.chunk.js" as main
        file "favicon.ico" as favicon
        file "vendor~main.chunk.js" as vendor
        file "bundle.js" as bundle

        node_modules --> vendor
        src --> main
        public_favicon --> favicon
        public_manifest --> manifest

        artifact "index.html" as index {
            public_index --> index
            manifest --> index
            main --> index
            favicon --> index
            vendor --> index
            bundle -r-> index
        }
    }
}
@enduml
```

#### Пример таблицы

№ | attribute | description
--- | ---: | :---:
_1_ | Id | Идентификатор
2 | name | Название
3 | status | Статус


[1]: https://www.youtube.com/watch?v=FFBTGdEMrQ4