# Базы данных, их типы

**Перваков Олег**

## Решения заданий

### Задание 1
1.1. Для этой задачи лучше всего подойдет реляционная СУБД, РСУБД обеспечивают целостность данных, поддержку транзакций, сложные аналитические запросы и возможности для создания отчётов
1.2 Для лендингов, где важна высокая скорость обработки запросов и гибкость структуры данных, лучше использовать NoSQL базы данных, такие как MongoDB, Для CRM можно использовать РСУБД ,так как здесь важна структурированность данных, поддержка транзакций и аналитических запросов.
1.3 Для такой задачи лучше всего подойдет реляционная СУБД с простой структурой, например, MySQL, она обеспечит простоту использования и хорошую структуру данных для хранения корпоративных документов, учебных материалов и другой подобной информации
1.4 Для логистики, где требуется быстрое построение связей между объектами, лучше использовать графовую СУБД, графовые базы данных обеспечивают эффективное управление и обработку данных, связанных с маршрутами и связями между объектами
1.4* Отдел закупок можно подключить к той же графовой СУБД, если их задачи пересекаются с задачами логистов, если задачи закупок требуют обработки других типов данных, можно использовать отдельную реляционную СУБД и связать её с графовой
1.5  Все задачи можно решить с помощью одной PostgreSQL благодаря её гибкости и расширяемости, однако это решение может потребовать значительных настроек и не будет таким оптимальным, как использование специализированных СУБД для каждой задачи
### Задание 2
1-Система проверяет, есть ли на счёте пользователя достаточно средств для проведения операции, если средств недостаточно, транзакция отклоняется
2-После подтверждения наличия средств, система временно замораживает необходимую сумму на счёте пользователя, чтобы исключить возможность их использования в других транзакциях до завершения текущей операции
3-В базе данных создается запись о транзакции, которая включает информацию о сумме пополнения, идентификаторе пользователя, времени и других необходимых параметрах
4-Система увеличивает баланс телефона на указанную сумму, это действие также записывается в базе данных
5-Если все предыдущие шаги выполнены успешно, система снимает заморозку средств на счёте пользователя и окончательно списывает средства
6-Система отправляет пользователю уведомление о успешном пополнении баланса, в случае успеха, статус транзакции обновляется на завершено
### Задание 3
1 преимущество - Строгая схема данных и целостность: SQL-системы используют четко определенные схемы данных, что обеспечивает структурированность и целостность данных
2 преимущество - Поддержка сложных запросов и транзакций: SQL поддерживает сложные многоуровневые запросы,также SQL-системы обеспечивают полную поддержку транзакций с ACID-свойствами
3 преимущество - Стандартность и совместимость: SQL является международным стандартом для управления реляционными базами данных,стандартный синтаксис SQL понятен и поддерживается многими реляционными СУБД
4 преимущество - Зрелость и обширная экосистема: SQL-системы существуют уже несколько десятилетий и имеют обширную экосистему инструментов, библиотек и фреймворков, а также огромное количество документации и сообществ разработчиков,это облегчает обучение, разработку и поддержку
5 преимущество - Надежность и стабильность:SQL-системы проверены временем в различных индустриях и масштабах,они известны своей надежностью и стабильностью
6-Система отправляет пользователю уведомление о успешном пополнении баланса, в случае успеха, статус транзакции обновляется на завершено
### Задание 4
При выборе типа СУБД для данной задачи я опираюсь на критерий горизонтальной масштабируемости:СУБД должна эффективно масштабироваться горизонтально, то есть поддерживать распределение данных и вычислений на большое количество узлов,это позволит равномерно распределить нагрузку на все 1000 машин и обеспечить высокую производительность
Для задачи, требующей распределённой обработки больших объемов данных на 1000 машинах, наилучшим образом подойдёт модель Apache Spark, юлагодаря ее горизонтальной масштабируемости - Apache Spark масштабируется горизонтально и эффективно использует распределенные вычислительные ресурсы, что делает его отличным выбором для работы на кластере из 1000 машин
