# Task-Tracker
A CLI application to manage tasks.

Описание:

Task Tracker — это приложение с интерфейсом командной строки (CLI), разработанное для эффективного управления задачами. Это приложение позволяет пользователям добавлять, удалять, обновлять, перечислять задачи и управлять ими с помощью различных команд. Оно обеспечивает простой способ взаимодействия с базой данных задач с помощью простого интерфейса CLI, что делает его идеальным инструментом как для личного, так и для профессионального отслеживания задач.

Функции:

Task Tracker предлагает ряд функций, которые позволяют пользователям эффективно управлять своими задачами:

Добавить задачу : пользователи могут добавлять новую задачу в свой список задач, предоставляя описание. Каждой задаче присваивается уникальный идентификатор, и изначально ей присваивается статус «todo».
Удалить задачу : задачи можно удалить из списка, указав их уникальный идентификатор.
Обновить задачу : Описание существующей задачи может быть обновлено. Для этого требуется идентификатор задачи и новое описание.
Список задач : пользователи могут перечислить все задачи или отфильтровать их по статусу. Статусы, доступные для фильтрации: «все», «done», «todo» и «in-progress».
Отметить задачу как выполняемую : задачи можно пометить как выполняемые («in-progress»), указав их идентификатор.
Отметить задачу как выполненную : задачи можно пометить как выполненные («done»), указав их идентификатор.

Структура проекта:

task_cli.py : Это основной файл, содержащий реализацию приложения. Он включает:

main(): Точка входа приложения, которая обрабатывает аргументы командной строки и вызывает соответствующие функции
adding(task_name: str): Добавляет новую задачу в базу данных.
deletion(id: str): Удаляет задачу из базы данных.
updating(id: str, new_name: str): Обновляет название или описание задачи.
show_list(): Список всех задач.
show_todo(): Список не начатых задач.
show_in_progress(): Список задач в процессе выполнения.
show_done(): Список выполненных задач.
mark_in_progress(id: str): Помечает задачу как «в процессе выполнения».
mark_done(id: str): Отмечает задачу как «выполненную».

Установка и использование

Установка : можно выполнить через pip
pip install <директория>

Использование : Теперь вы можете запустить Task Tracker из командной строки. Вот примеры запуска со всеми возможными командами:

$ task-cli add "task_name"                                                  # Добавить задачу

$ task-cli update 1 "task_name"                                             # Обновить задачу

$ task-cli mark-done 1                                                      # Отметить задачу как выполненную

$ task-cli mark-in-progress 1                                               # Отметить задачу как выполняемую (в процессе)

$ task-cli list                                                             # Список всех задач

$ task-cli list done                                                        # Список выполненных

$ task-cli list todo                                                        # Список запланированных

$ task-cli list in-progress                                                 # Список задач в процессе выполнения

$ task-cli delete 1                                                         # Удалить задачу
