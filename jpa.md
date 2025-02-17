[Вопросы для собеседования](README.md)

# JPA (Java Persistence API)
+ [Что такое JPA?](#Что-такое-JPA)
+ [Из чего состоит JPA?](#Из-чего-состоит-JPA)
+ [В чем её отличие JPA от Hibernate?](#В-чем-её-отличие-JPA-от-Hibernate)
+ [В чем её отличие JPA от JDO?](#В-чем-её-отличие-JPA-от-JDO)
+ [Можно ли использовать JPA c noSQL базами?](#Можно-ли-использовать-JPA-c-noSQL-базами)
+ [Что такое JPQL (Java Persistence query language) и чем он отличается от SQL?](#Что-такое-JPQL-Java-Persistence-query-language-и-чем-он-отличается-от-SQL)
+ [Что означает полиморфизм (polymorphism) в запросах JPQL (Java Persistence query language) и как его "выключить"?](#Что-означает-полиморфизм-polymorphism-в-запросах-JPQL-Java-Persistence-query-language-и-как-его-выключить)
+ [Что такое Criteria API и для чего он используется?](#Что-такое-Criteria-API-и-для-чего-он-используется)
+ [Что такое Entity?](#Что-такое-Entity)
+ [Может ли не Entity класс наследоваться от Entity класса?](#Может-ли-не-Entity-класс-наследоваться-от-Entity-класса)
+ [Может ли Entity класс наследоваться от других Entity классов?](#Может-ли-Entity-класс-наследоваться-от-других-Entity-классов)
+ [Может ли Entity быть абстрактным классом?](#Может-ли-Entity-быть-абстрактным-классом)
+ [Может ли Entity класс наследоваться от не Entity классов (non-entity classes)?](#Может-ли-Entity-класс-наследоваться-от-не-Entity-классов-non-entity-classes)
+ [Какие требования JPA к Entity классам вы можете перечислить (не менее шести требований)?](#Какие-требования-JPA-к-Entity-классам-вы-можете-перечислить-не-менее-шести-требований)
+ [Что такое атрибут Entity класса в терминологии JPA?](#Что-такое-атрибут-Entity-класса-в-терминологии-JPA)
+ [Какие два типа элементов есть у Entity классов. Или другими словами перечислите два типа доступа (access) к элементам Entity классов.](#Какие-два-типа-элементов-есть-у-Entity-классов-Или-другими-словами-перечислите-два-типа-доступа-access-к-элементам-Entity-классов)
+ [Какие типы данных допустимы в атрибутах Entity класса (полях или свойствах)?](#Какие-типы-данных-допустимы-в-атрибутах-Entity-класса-полях-или-свойствах)
+ [Какие типы данных можно использовать в атрибутах, входящих в первичный ключ Entity класса (составной или простой), чтобы полученный первичный ключ мог использоваться для любой базы данных? А в случае автогенерируемого первичного ключа (generated primary keys)?](#Какие-типы-данных-можно-использовать-в-атрибутах-входящих-в-первичный-ключ-Entity-класса-составной-или-простой-чтобы-полученный-первичный-ключ-мог-использоваться-для-любой-базы-данных-А-в-случае-автогенерируемого-первичного-ключа-generated-primary-keys)
+ [Что такое встраиваемый (Embeddable) класс?](#Что-такое-встраиваемый-Embeddable-класс)
+ [Может ли встраиваемый (Embeddable) класс содержать другой встраиваемый (Embeddable) класс?](#Может-ли-встраиваемый-Embeddable-класс-содержать-другой-встраиваемый-Embeddable-класс)
+ [Может ли встраиваемый (Embeddable) класс содержать связи (relationship) с другими Entity или коллекциями Entity? Если может, то существуют ли какие-то ограничение на такие связи (relationship)?](#Может-ли-встраиваемый-Embeddable-класс-содержать-связи-relationship-с-другими-Entity-или-коллекциями-Entity-Если-может-то-существуют-ли-какие-то-ограничение-на-такие-связи-relationship)
+ [Какие требования JPA устанавливает к встраиваемым (Embeddable) классам?](#Какие-требования-JPA-устанавливает-к-встраиваемым-Embeddable-классам)
+ [Какие типы связей (relationship) между Entity вы знаете (перечислите восемь типов, либо укажите четыре типа связей, каждую из которых можно разделить ещё на два вида)?](#Какие-типы-связей-relationship-между-Entity-вы-знаете-перечислите-восемь-типов-либо-укажите-четыре-типа-связей-каждую-из-которых-можно-разделить-ещё-на-два-вида)
+ [Что такое Mapped Superclass?](#Что-такое-Mapped-Superclass)
+ [Какие два типа fetch стратегии в JPA вы знаете?](#Какие-два-типа-fetch-стратегии-в-JPA-вы-знаете)
+ [Какие три типы стратегии наследования мапинга (Inheritance Mapping Strategies) описаны в JPA?](#Какие-три-типы-стратегии-наследования-мапинга-Inheritance-Mapping-Strategies-описаны-в-JPA)

+ [Что такое EntityManager и какие основные его функции вы можете перечислить?](#Что-такое-EntityManager-и-какие-основные-его-функции-вы-можете-перечислить)
+ [Какие четыре статуса жизненного цикла Entity объекта (Entity Instance’s Life Cycle) вы можете перечислить?](#Какие-четыре-статуса-жизненного-цикла-Entity-объекта-Entity-Instance’s-Life-Cycle-вы-можете-перечислить)
+ [Как влияет операция merge на Entity объекты каждого из четырех статусов?](#Как-влияет-операция-merge-на-Entity-объекты-каждого-из-четырех-статусов)
+ [Как влияет операция remove на Entity объекты каждого из четырех статусов?](#Как-влияет-операция-remove-на-Entity-объекты-каждого-из-четырех-статусов)
+ [Как влияет операция persist на Entity объекты каждого из четырех статусов?](#Как-влияет-операция-persist-на-Entity-объекты-каждого-из-четырех-статусов)
+ [Как влияет операция refresh на Entity объекты каждого из четырех статусов?](#Как-влияет-операция-refresh-на-Entity-объекты-каждого-из-четырех-статусов)
+ [Как влияет операция detach на Entity объекты каждого из четырех статусов?](#Как-влияет-операция-detach-на-Entity-объекты-каждого-из-четырех-статусов)
+ [Для чего нужна аннотация Access?](#Для-чего-нужна-аннотация-Access)
+ [Для чего нужна аннотация Basic?](#Для-чего-нужна-аннотация-Basic)
+ [Какой аннотациями можно перекрыть связи (override entity relationship) или атрибуты, унаследованные от суперкласса, или заданные в embeddable классе при использовании этого embeddable класса в одном из entity классов и не перекрывать в остальных?](#Какой-аннотациями-можно-перекрыть-связи-override-entity-relationship-или-атрибуты-унаследованные-от-суперкласса-или-заданные-в-embeddable-классе-при-использовании-этого-embeddable-класса-в-одном-из-entity-классов-и-не-перекрывать-в-остальных)
+ [Какие аннотации служит для задания класса преобразования basic атрибута Entity в другой тип при сохранении/получении данных их базы (например, работать с атрибутом Entity boolean типа, но в базу сохранять его как число)?](#Какие-аннотации-служит-для-задания-класса-преобразования-basic-атрибута-Entity-в-другой-тип-при-сохранении/получении-данных-их-базы-например-работать-с-атрибутом-Entity-boolean-типа-но-в-базу-сохранять-его-как-число)
+ [Какой аннотацией можно управлять кешированием JPA для данного Entity?](#Какой-аннотацией-можно-управлять-кешированием-JPA-для-данного-Entity)
+ [Какой аннотацией можно задать класс, методы которого должен выполнится при определенных JPA операциях над данным Enitity или Mapped Superclass (такие как удаление, изменение данных и т.п.)?](#Какой-аннотацией-можно-задать-класс-методы-которого-должен-выполнится-при-определенных-JPA-операциях-над-данным-Enitity-или-Mapped-Superclass-такие-как-удаление-изменение-данных-и-тп)
+ [Для чего нужны callback методы в JPA? К каким сущностям применяются аннотации callback методов? Перечислите семь callback методов (или что тоже самое аннотаций callback методов).](#Для-чего-нужны-callback-методы-в-JPA-К-каким-сущностям-применяются-аннотации-callback-методов-Перечислите-семь-callback-методов-или-что-тоже-самое-аннотаций-callback-методов)
+ [Какой аннотацей можно исключить поли и свойства Entity из маппинга (property or field is not persistent)?](#Какой-аннотацей-можно-исключить-поли-и-свойства-Entity-из-маппинга-property-or-field-is-not-persistent)
+ [Какие аннотации служить для установки порядка выдачи элементов коллекций Entity?](#Какие-аннотации-служить-для-установки-порядка-выдачи-элементов-коллекций-Entity)
+ [Какие шесть видов блокировок (lock) описаны в спецификации JPA (или какие есть значения у enum LockModeType в JPA)?](#Какие-шесть-видов-блокировок-lock-описаны-в-спецификации-JPA-или-какие-есть-значения-у-enum-LockModeType-в-JPA)
+ [Какие два вида кэшей (cache) вы знаете в JPA и для чего они нужны?](#Какие-два-вида-кэшей-cache-вы-знаете-в-JPA-и-для-чего-они-нужны)
+ [Какие есть варианты настройки second-level cache (кэша второго уровня) в JPA или что аналогично опишите какие значения может принимать элемент shared-cache-mode из persistence.xml?](#Какие-есть-варианты-настройки-second-level-cache-кэша-второго-уровня-в-JPA-или-что-аналогично-опишите-какие-значения-может-принимать-элемент-shared-cache-mode-из-persistencexml)
+ [Как можно изменить настройки fetch стратегии любых атрибутов Entity для отдельных запросов (query) или методов поиска (find), то если у Enity есть атрибут с fetchType = LAZY, но для конкретного запроса его требуется сделать EAGER или наоборот?](#Как-можно-изменить-настройки-fetch-стратегии-любых-атрибутов-Entity-для-отдельных-запросов-query-или-методов-поиска-find-то-если-у-Enity-есть-атрибут-с-fetchType-=-LAZY-но-для-конкретного-запроса-его-требуется-сделать-EAGER-или-наоборот)
+ [Каким способом можно получить метаданные JPA (сведения о Entity типах, Embeddable и Managed классах и т.п.)?](#Каким-способом-можно-получить-метаданные-JPA-сведения-о-Entity-типах-Embeddable-и-Managed-классах-и-тп)
+ [Каким способом можно в коде работать с кэшем второго уровня (удалять все или определенные Entity из кеша, узнать закэшировался ли данное Entity и т.п.)?](#Каким-способом-можно-в-коде-работать-с-кэшем-второго-уровня-удалять-все-или-определенные-Entity-из-кеша-узнать-закэшировался-ли-данное-Entity-и-тп)
+ [В чем разница в требованиях к Entity в Hibernate, от требований к Entity, указанных в спецификации JPA?](#В-чем-разница-в-требованиях-к-Entity-в-Hibernate-от-требований-к-Entity-указанных-в-спецификации-JPA)
+ [Какая уникальная стратегия наследования есть в Hibernate, но нет в спецификации JPA?](#Какая-уникальная-стратегия-наследования-есть-в-Hibernate-но-нет-в-спецификации-JPA)
+ [Какие основные новые возможности появились в спецификации JPA 2.1 по сравнению с JPA 2.0 (перечислите хотя бы пять-шесть новых возможностей)?](#Какие-основные-новые-возможности-появились-в-спецификации-JPA-21-по-сравнению-с-JPA-20-перечислите-хотя-бы-пять-шесть-новых-возможностей)



## Что такое JPA?

JPA - это технология, обеспечивающая объектно-реляционное отображение простых JAVA объектов и предоставляющая API для сохранения, получения и управления такими объектами.
JPA - это спецификация (документ, утвержденный как стандарт, описывающий все аспекты технологии), часть EJB3 спецификации.
Сам JPA не умеет ни сохранять, ни управлять объектами, JPA только определяет правила игры: как что-то будет действовать. JPA также определяет интерфейсы, которые должны будут быть реализованы провайдерами. Плюс к этому JPA определяет правила о том, как должны описываться метаданные отображения и о том, как должны работать провайдеры. Дальше, каждый провайдер, реализуя JPA определяет получение, сохранение и управление объектами. У каждого провайдера реализация разная.
+ Реализации JPA:
+ Hibernate
+ Oracle TopLink
+ Apache OpenJPA

## Из чего состоит JPA?

JPA состоит из трех основных пунктов:
+ API - интерфейсы в пакете javax.persistance. Набор интерфейсов, которые позволяют организовать взаимодействие с ORM провайдером.
+ JPQL - объектный язык запросов. Очень похож на SQL, но запросы выполняются к объектам.
+ Metadata - аннотации над объектами. Набор аннотаций, которыми мы описываем метаданные отображения. Тогда уже JPA знает какой объект в какую таблицу нужно сохранить. Метаданные можно описывать двумя способами: XML-файлом или через аннотации.

## В чем её отличие JPA от Hibernate?

Hibernate одна из самых популярных открытых реализаций последней версии спецификации (JPA 2.1). То есть JPA только описывает правила и API, а Hibernate реализует эти описания, впрочем у Hibernate (как и у многих других реализаций JPA) есть дополнительные возможности, не описанные в JPA (и не переносимые на другие реализации JPA).

## В чем её отличие JPA от JDO?

JPA (Java Persistence API) и Java Data Objects (JDO) две спецификации сохранения java объектов в базах данных. Если JPA сконцентрирована только на реляционных базах, то JDO более общая спецификация которая описывает ORM для любых возможных баз и хранилищ. Также отличаются "разработчики" спецификаций - если JPA разрабатывается как JSR, то JDO сначала разрабатывался как JSR, теперь разрабатывается как проект Apache JDO.

## Можно ли использовать JPA c noSQL базами?

Спецификация JPA говорит только о отображении java объектов в таблицы реляционных баз данных, но при этом существует ряд реализаций данного стандарта для noSql баз данных: Kundera, DataNucleus, ObjectDB и ряд других. Естественно, при это не все специфичные для реляционных баз данных особенности спецификации переносятся при этом на nosql базы полностью.

## Что такое JPQL (Java Persistence query language) и чем он отличается от SQL?

JPQL (Java Persistence query language) это язык запросов, практически такой же как SQL, однако вместо имен и колонок таблиц базы данных, он использует имена классов Entity и их атрибуты. В качестве параметров запросов так же используются типы данных атрибутов Entity, а не полей баз данных. В отличии от SQL в JPQL есть автоматический полиморфизм. Также в JPQL используется функции которых нет в SQL: такие как KEY (ключ Map’ы), VALUE (значение Map’ы), TREAT (для приведение суперкласса к его объекту-наследнику, downcasting), ENTRY и т.п.

## Что означает полиморфизм (polymorphism) в запросах JPQL (Java Persistence query language) и как его "выключить"?

В отличии от SQL в запросах JPQL есть автоматический полиморфизм, то есть каждый запрос к Entity возвращает не только объекты этого Entity, но так же объекты всех его классов-потомков, независимо от стратегии наследования (например, запрос select * from Animal, вернет не только объекты Animal, но и объекты классов Cat и Dog, которые унаследованы от Animal). Чтобы исключить такое поведение используется функция TYPE в where условии (например select * from Animal a where TYPE(a) IN (Animal, Cat) уже не вернет объекты класса Dog).

## Что такое Criteria API и для чего он используется?

Criteria API это тоже язык запросов, аналогичным JPQL (Java Persistence query language), однако запросы основаны на методах и объектах, то есть запросы выглядят так:


## Что такое Entity?

Entity это легковесный хранимый объект бизнес логики (persistent domain object). Основная программная сущность это entity класс, который так же может использовать дополнительные классы, который могут использоваться как вспомогательные классы или для сохранения состояния еntity.

## Может ли не Entity класс наследоваться от Entity класса?

Может.

## Может ли Entity класс наследоваться от других Entity классов?

Может.

## Может ли Entity быть абстрактным классом?

Может, при этом он сохраняет все свойства Entity, за исключением того что его нельзя непосредственно инициализировать.

## Может ли Entity класс наследоваться от не Entity классов (non-entity classes)?

Может.


## Какие требования JPA к Entity классам вы можете перечислить (не менее шести требований)?

1.&nbsp;Entity класс должен быть отмечен аннотацией Entity или описан в XML файле конфигурации JPA.
2.&nbsp;Entity класс должен содержать public или protected конструктор без аргументов (он также может иметь конструкторы с аргументами).
3.&nbsp;Entity класс должен быть классом верхнего уровня (top-level class).
4.&nbsp;Entity класс не может быть enum или интерфейсом.
5.&nbsp;Entity класс не может быть финальным классом (final class).
6.&nbsp;Entity класс не может содержать финальные поля или методы, если они участвуют в маппинге (persistent final methods or persistent final instance variables).
7.&nbsp;Если объект Entity класса будет передаваться по значению как отдельный объект (detached object), например через удаленный интерфейс (through a remote interface), он так же должен реализовывать Serializable интерфейс.
8.&nbsp;Поля Entity класс должны быть напрямую доступны только методам самого Entity класса и не должны быть напрямую доступны другим классам, использующим этот Entity. Такие классы должны обращаться только к методам (getter/setter методам или другим методам бизнес-логики в Entity классе).
9.&nbsp;Enity класс должен содержать первичный ключ, то есть атрибут или группу атрибутов которые уникально определяют запись этого Enity класса в базе данных.


## Что такое атрибут Entity класса в терминологии JPA?

JPA указывает что она может работать как с свойствами классов (property), оформленные в стиле JavaBeans, либо с полями (field), то есть переменными класса (instance variables). Оба типа элементов Entity класса называются атрибутами Entity класса.

## Какие два типа элементов есть у Entity классов. Или другими словами перечислите два типа доступа (access) к элементам Entity классов.

JPA указывает что она может работать как с свойствами классов (property), оформленные в стиле JavaBeans, либо с полями (field), то есть переменными класса (instance variables). Соответственно, при этом тип доступа будет либо property access или field access.

## Какие типы данных допустимы в атрибутах Entity класса (полях или свойствах)?

Допустимые типы атрибутов у Entity классов:
+ примитивные типы и их обертки Java,
+ строки,
+ любые сериализуемые типы Java (реализующие Serializable интерфейс),
+ enums;
+ entity types;
+ embeddable классы
+ и коллекции типов 1-6

## Какие типы данных можно использовать в атрибутах, входящих в первичный ключ Entity класса (составной или простой), чтобы полученный первичный ключ мог использоваться для любой базы данных? А в случае автогенерируемого первичного ключа (generated primary keys)?

Допустимые типы атрибутов, входящих в первичный ключ:
+ примитивные типы и их обертки Java,
+ строки,
+ BigDecimal и BigInteger,
+ java.util.Date и java.sql.Date,В случае автогенерируемого первичного ключа (generated primary keys) допустимы&nbsp;только числовые типы,В случае использования других типов данных в первичном ключе, он может работать только для некоторых баз данных, т.е. становится не переносимым (not portable).

## Что такое встраиваемый (Embeddable) класс?

Встраиваемый (Embeddable) класс это класс который не используется сам по себе, только как часть одного или нескольких Entity классов. Entity класс могут содержать как одиночные встраиваемые классы, так и коллекции таких классов. Также такие классы могут быть использованы как ключи или значения map. Во время выполнения каждый встраиваемый класс принадлежит только одному объекту Entity класса и не может быть использован для передачи данных между объектами Entity классов (то есть такой класс не является общей структурой данных для разных объектов). В целом, такой класс служит для того чтобы выносить определение общих атрибутов для нескольких Entity, можно считать что JPA просто встраивает в Entity вместо объекта такого класса те атрибуты, которые он содержит.

## Может ли встраиваемый (Embeddable) класс содержать другой встраиваемый (Embeddable) класс?

Да, может.

## Может ли встраиваемый (Embeddable) класс содержать связи (relationship) с другими Entity или коллекциями Entity? Если может, то существуют ли какие-то ограничение на такие связи (relationship)?

Может, но только в случае если такой класс не используется как первичный ключ или ключ map’ы.

## Какие требования JPA устанавливает к встраиваемым (Embeddable) классам?

1. Такие классы должны удовлетворять тем же правилам что Entity классы, за исключением того что они не обязаны содержать первичный ключ и быть отмечены аннотацией Entity
2. Embeddable класс должен быть отмечен аннотацией Embeddable или описан в XML файле конфигурации JPA.

## Какие типы связей (relationship) между Entity вы знаете (перечислите восемь типов, либо укажите четыре типа связей, каждую из которых можно разделить ещё на два вида)?

Существуют следующие четыре типа связей
+ OneToOne (связь один к одному, то есть один объект Entity может связан не больше чем с один объектом другого Entity ),
+ OneToMany (связь один ко многим, один объект Entity может быть связан с целой коллекцией других Entity),
+ ManyToOne (связь многие к одному, обратная связь для OneToMany),
+ ManyToMany (связь многие ко многим).
Каждую из которых можно разделить ещё на два вида:
+ Bidirectional - ссылка на связь устанавливается у всех Entity, то есть в случае OneToOne A-B в Entity A есть ссылка на Entity B, в Entity B есть ссылка на Entity A, Entity A считается владельцем этой связи (это важно для случаев каскадного удаления данных, тогда при удалении A также будет удалено B, но не наоборот).
+ Undirectional - ссылка на связь устанавливается только с одной стороны, то есть в случае OneToOne A-B только у Entity A будет ссылка на Entity B, у Entity B ссылки на A не будет.

## Что такое Mapped Superclass?

Mapped Superclass это класс от которого наследуются Entity, он может содержать аннотации JPA, однако сам такой класс не является Entity, ему не обязательно выполнять все требования установленные для Entity (например, он может не содержать первичного ключа). Такой класс не может использоваться в операциях EntityManager или Query. Такой класс должен быть отмечен аннотацией MappedSuperclass или соответственно описан в xml файле.

## Какие два типа fetch стратегии в JPA вы знаете?

В JPA описаны два типа fetch стратегии:
+ LAZY - данные поля будут загружены только во время первого доступа к этому полю,
+ EAGER - данные поля будут загружены немедленно.

## Какие три типы стратегии наследования мапинга (Inheritance Mapping Strategies) описаны в JPA?

В JPA описаны три стратегии наследования мапинга (Inheritance Mapping Strategies), то есть как JPA будет работать с классами-наследниками Entity:
+ одна таблица на всю иерархию наследования (a single table per class hierarchy) - все enity, со всеми наследниками записываются в одну таблицу, для идентификации типа entity определяется специальная колонка "discriminator column". Например, если есть entity Animals c классами-потомками Cats и Dogs, при такой стратегии все entity записываются в таблицу Animals, но при это имеют дополнительную колонку animalType в которую соответственно пишется значение "cat" или "dog".Минусом является то что в общей таблице, будут созданы все поля уникальные для каждого из классов-потомков, которые будет пусты для всех других классов-потомков. Например, в таблице animals окажется и скорость лазанья по дереву от cats и может ли пес приносить тапки от dogs, которые будут всегда иметь null для dog и cat соответственно.
+ объединяющая стратегия (joined subclass strategy) - в этой стратегии каждый класс enity сохраняет данные в свою таблицу, но только уникальные колонки (не унаследованные от классов-предков) и первичный ключ, а все унаследованные колонки записываются в таблицы класса-предка, дополнительно устанавливается связь (relationships) между этими таблицами, например в случае классов Animals (см.выше), будут три таблицы animals, cats, dogs, причем в cats будет записана только ключ и скорость лазанья, в dogs - ключ и умеет ли пес приносить палку, а в animals все остальные данные cats и dogs c ссылкой на соответствующие таблицы. Минусом тут являются потери производительности от объединения таблиц (join) для любых операций.
+ одна таблица для каждого класса (table per concrete class strategy) - тут все просто каждый отдельный класс-наследник имеет свою таблицу, т.е. для cats и dogs все данные будут записываться просто в таблицы cats и dogs как если бы они вообще не имели общего суперкласса. Минусом является плохая поддержка полиморфизма (polymorphic relationships) и то что для выборки всех классов иерархии потребуются большое количество отдельных sql запросов или использование UNION запроса.

Часть II


## Что такое EntityManager и какие основные его функции вы можете перечислить?

EntityManager это интерфейс, который описывает API для всех основных операций над Enitity, получение данных и других сущностей JPA. По сути главный API для работы с JPA. Основные операции:
+ Для операций над Entity: persist (добавление Entity под управление JPA), merge (обновление), remove (удаления), refresh (обновление данных), detach (удаление из управление JPA), lock (блокирование Enity от изменений в других thread),
+ Получение данных: find (поиск и получение Entity), createQuery, createNamedQuery, createNativeQuery, contains, createNamedStoredProcedureQuery, createStoredProcedureQuery
+ Получение других сущностей JPA: getTransaction, getEntityManagerFactory, getCriteriaBuilder, getMetamodel, getDelegate
+ Работа с EntityGraph: createEntityGraph, getEntityGraph
+ Общие операции над EntityManager или всеми Entities: close, isOpen, getProperties, setProperty, clear.

## Какие четыре статуса жизненного цикла Entity объекта (Entity Instance’s Life Cycle) вы можете перечислить?

У Entity объекта существует четыре статуса жизненного цикла: new, managed, detached, или removed. Их описание
+ new - объект создан, но при этом ещё не имеет сгенерированных первичных ключей и пока ещё не сохранен в базе данных,
+ managed - объект создан, управляется JPA, имеет сгенерированные первичные ключи,
+ detached - объект был создан, но не управляется (или больше не управляется) JPA,
+ removed - объект создан, управляется JPA, но будет удален после commit’a транзакции.

## Как влияет операция merge на Entity объекты каждого из четырех статусов?

1. Если статус detached, то либо данные будет скопированы в существующей managed entity с тем же первичным ключом, либо создан новый managed в который скопируются данные,
2. Если статус Entity new, то будет создана новый managed entity, в который будут скопированы данные прошлого объекта,
3. Если статус managed, операция игнорируется, однако операция merge сработает на каскадно зависимые Entity, если их статус не managed,
4. Если статус removed, будет выкинут exception сразу или на этапе commit’а транзакции.

## Как влияет операция remove на Entity объекты каждого из четырех статусов?

1. Если статус Entity new, операция игнорируется, однако зависимые Entity могут поменять статус на removed, если у них есть аннотации каскадных изменений и они имели статус managed,
2. Если статус managed, то статус меняется на removed и запись объект в базе данных будет удалена при commit’е транзакции (так же произойдут операции remove для всех каскадно зависимых объектов),
3. Если статус removed, то операция игнорируется,
4. Если статус detached, будет выкинут exception сразу или на этапе commit’а транзакции.

## Как влияет операция persist на Entity объекты каждого из четырех статусов?

1. Если статус Entity new, то он меняется на managed и объект будет сохранен в базу при commit’е транзакции или в результате flush операций,
2. Если статус уже managed, операция игнорируется, однако зависимые Entity могут поменять статус на managed, если у них есть аннотации каскадных изменений,
3. Если статус removed, то он меняется на managed,
4. Если статус detached, будет выкинут exception сразу или на этапе commit’а транзакции.

## Как влияет операция refresh на Entity объекты каждого из четырех статусов?

1. Если статус Entity managed, то в результате операции будут востановленны все изменения из базы данных данного Entity, так же произойдет refresh всех каскадно зависимых объектов,
2. Если статус new, removed или detached, будет выкинут exception.

## Как влияет операция detach на Entity объекты каждого из четырех статусов?

1. Если статус Entity managed или removed, то в результате операции статус Entity (и всех каскадно-зависимых объектов) станет detached.
2. Если статус new или detached, то операция игнорируется.

## Для чего нужна аннотация Access?

Она определяет тип доступа (access type) для класса entity, суперкласса, embeddable или отдельных атрибутов, то есть как JPA будет обращаться к атрибутам entity, как к полям класса (FIELD) или как к свойствам класса (PROPERTY), имеющие гетеры (getter) и сетеры (setter).

## Для чего нужна аннотация Basic?

Basic - указывает на простейший тип маппинга данных на колонку таблицы базы данных. Также в параметрах аннотации можно указать fetch стратегию доступа к полю и является ли это поле обязательным или нет.

## Какой аннотациями можно перекрыть связи (override entity relationship) или атрибуты, унаследованные от суперкласса, или заданные в embeddable классе при использовании этого embeddable класса в одном из entity классов и не перекрывать в остальных?

Для такого перекрывания существует четыре аннотации:
+ AttributeOverride чтобы перекрыть поля, свойства и первичные ключи,
+ AttributeOverrides аналогично можно перекрыть поля, свойства и первичные ключи со множественными значениями,
+ AssociationOverride чтобы перекрывать связи (override entity relationship),
+ AssociationOverrides чтобы перекрывать множественные связи (multiple relationship).
 

## Какие аннотации служит для задания класса преобразования basic атрибута Entity в другой тип при сохранении/получении данных их базы (например, работать с атрибутом Entity boolean типа, но в базу сохранять его как число)?

Convert и Converts - позволяют указать класс для конвертации Basic атрибута Entity в другой тип (Converts - позволяют указать несколько классов конвертации). Классы для конвертации должны реализовать интерфейс AttributeConverter и могут быть отмечены (но это не обязательно) аннотацией Converter.

## Какой аннотацией можно управлять кешированием JPA для данного Entity?

Cacheable - позволяет включить или выключить использование кеша второго уровня (second-level cache) для данного Entity (если провайдер JPA поддерживает работу с кешированием и настройки кеша (second-level cache) стоят как ENABLE_SELECTIVE или DISABLE_SELECTIVE, см вопрос 41). Обратите внимание свойство наследуется и если не будет перекрыто у наследников, то кеширование измениться и для них тоже.

## Какой аннотацией можно задать класс, методы которого должен выполнится при определенных JPA операциях над данным Enitity или Mapped Superclass (такие как удаление, изменение данных и т.п.)?

Аннотация EntityListeners позволяет задать класс Listener, который будет содержать методы обработки событий (сallback methods) определенных Entity или Mapped Superclass.

## Для чего нужны callback методы в JPA? К каким сущностям применяются аннотации callback методов? Перечислите семь callback методов (или что тоже самое аннотаций callback методов).

Callback методы служат для вызова при определенных событиях Entity (то есть добавить обработку например удаления Entity методами JPA), могут быть добавлены к entity классу, к mapped superclass, или к callback listener классу, заданному аннотацией EntityListeners (см предыдущий вопрос). Существует семь callback методов (и аннотаций с теми же именами):
+ PrePersist
+ PostPersist
+ PreRemove
+ PostRemove
+ PreUpdate
+ PostUpdate
+ PostLoad

## Какой аннотацей можно исключить поли и свойства Entity из маппинга (property or field is not persistent)?

Для этого служит аннотация Transient.

## Какие аннотации служить для установки порядка выдачи элементов коллекций Entity?

Для этого служит аннотация OrderBy и OrderColumn.

## Какие шесть видов блокировок (lock) описаны в спецификации JPA (или какие есть значения у enum LockModeType в JPA)?

У JPA есть шесть видов блокировок, перечислим их в порядке увеличения надежности (от самого ненадежного и быстрого, до самого надежного и медленного):
+ NONE - без блокировки
+ OPTIMISTIC (или синоним READ, оставшийся от JPA 1) - оптимистическая блокировка
+ OPTIMISTIC_FORCE_INCREMENT (или синоним WRITE, оставшийся от JPA 1) - оптимистическая блокировка с принудительным увеличением поля версионности
+ PESSIMISTIC_READ - пессимистичная блокировка на чтение
+ PESSIMISTIC_WRITE - пессимистичная блокировка на запись (и чтение)
+ PESSIMISTIC_FORCE_INCREMENT - пессимистичная блокировка на запись (и чтение) с принудительным увеличением поля версионности.

## Какие два вида кэшей (cache) вы знаете в JPA и для чего они нужны?

JPA говорит о двух видов кэшей (cache):
+ first-level cache (кэш первого уровня) - кэширует данные одной транзакции,
+ second-level cache (кэш второго уровня) - кэширует данные дольше чем одна транзакция. Провайдер JPA может, но не обязан реализовывать работу с кэшем второго уровня. Такой вид кэша позволяет сэкономить время доступа и улучшить производительность, однако оборотной стороной является возможность получить устаревшие данные.

## Какие есть варианты настройки second-level cache (кэша второго уровня) в JPA или что аналогично опишите какие значения может принимать элемент shared-cache-mode из persistence.xml?

JPA говорит о пяти значениях shared-cache-mode из persistence.xml, который определяет как будет использоваться second-level cache:
+ ALL - все Entity могут кэшироваться в кеше второго уровня
+ NONE - кеширование отключено для всех Entity
+ ENABLE_SELECTIVE - кэширование работает только для тех Entity, у которых установлена аннотация Cacheable(true) или её xml эквивалент, для всех остальных кэширование отключено
+ DISABLE_SELECTIVE - кэширование работает для всех Entity, за исключением тех у которых установлена аннотация Cacheable(false) или её xml эквивалент
+ UNSPECIFIED - кеширование не определенно, каждый провайдер JPA использует свою значение по умолчанию для кэширования


## Как можно изменить настройки fetch стратегии любых атрибутов Entity для отдельных запросов (query) или методов поиска (find), то если у Enity есть атрибут с fetchType = LAZY, но для конкретного запроса его требуется сделать EAGER или наоборот?

Для этого существует EntityGraph API, используется он так: с помощью аннотации NamedEntityGraph для Entity, создаются именованные EntityGraph объекты, которые содержат список атрибутов у которых нужно поменять fetchType на EAGER, а потом данное имя указывается в hits запросов или метода find. В результате fetchType атрибутов Entity меняется, но только для этого запроса. Существует две стандартных property для указания EntityGraph в hit:
+ javax.persistence.fetchgraph - все атрибуты перечисленные в EntityGraph меняют fetchType на EAGER, все остальные на LAZY
+ javax.persistence.loadgraph - все атрибуты перечисленные в EntityGraph меняют fetchType на EAGER, все остальные сохраняют свой fetchType (то есть если у атрибута, не указанного в EntityGraph, fetchType был EAGER, то он и останется EAGER)С помощью NamedSubgraph можно также изменить fetchType вложенных объектов Entity.

## Каким способом можно получить метаданные JPA (сведения о Entity типах, Embeddable и Managed классах и т.п.)?

Для получения такой информации в JPA используется интерфейс Metamodel. Объект этого интерфейса можно получить методом getMetamodel у EntityManagerFactory или EntityManager.

## Каким способом можно в коде работать с кэшем второго уровня (удалять все или определенные Entity из кеша, узнать закэшировался ли данное Entity и т.п.)?

Для работы с кэшем второго уровня (second level cache) в JPA описан Cache интерфейс, содержащий большое количество методов по управлению кэшем второго уровня (second level cache), если он поддерживается провайдером JPA, конечно. Объект данного интерфейса можно получить с помощью метода getCache у EntityManagerFactory.

## В чем разница в требованиях к Entity в Hibernate, от требований к Entity, указанных в спецификации JPA?

1. Конструктор без аргументов не обязан быть public или protected, рекомендуется чтобы он был хотя бы package видимости, однако это только рекомендация, если настройки безопасности Java позволяют доступ к приватным полям, то он может быть приватным,
2. JPA категорически требует не использовать final классы, Hibernate лишь рекомендует не использовать такие классы чтобы он мог создавать прокси для ленивой загрузки, однако позволяет либо выключить прокси Proxy(lazy=false), либо использовать в качестве прокси интерфейс, содержащий все методы маппинга для данного класса (аннотацией Proxy(proxyClass=интерфейс.class) )

## Какая уникальная стратегия наследования есть в Hibernate, но нет в спецификации JPA?

В отличии JPA в Hibernate есть уникальная стратегия наследования, которая называется implicit polymorphism.
 

## Какие основные новые возможности появились в спецификации JPA 2.1 по сравнению с JPA 2.0 (перечислите хотя бы пять-шесть новых возможностей)?

В спецификации JPA 2.1 появились:
+ Entity Graphs - механизм динамического изменения fetchType для каждого запроса
+ Converters - механизм определения конвертеров для задания функций конвертации атрибутов Entity в поля базы данных
+ DDL генерация - автоматическая генерация таблиц, индексов и схем
+ Stored Procedures - механизм вызова хранимых процедур из JPA
+ Criteria Update/Delete - механизм вызова bulk updates или deletes, используя Criteria API
+ Unsynchronized persistence contexts - появление возможности указать SynchronizationType
+ Новые возможности в JPQL/Criteria API: арифметические подзапросы, generic database functions, join ON clause, функция TREAT
+ Динамическое создание именованных запросов (named queries)
+ Интерфейс EntityManager получил новые методы createStoredProcedureQuery, isJoinedToTransaction и createQuery(CriteriaUpdate или CriteriaDelete)
+ Абстрактный класс AbstractQuery стал наследоваться от класса CommonAbstractCriteria, появились новые интерфейсы CriteriaUpdate, CriteriaDelete унаследованные CommonAbstractCriteria,
+ PersistenceProvider получил новые функции generateSchema позволяющие генерить схемы,
+ EntityManagerFactory получил методы addNamedQuery, unwrap, addNamedEntityGraph, createEntityManager (с указанием SynchronizationType)
+ Появился новый enum SynchronizationType, Entity Graphs, StoredProcedureQuery и AttributeConverter интерфейсы.
