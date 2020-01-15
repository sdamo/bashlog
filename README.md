# Логирование событий для bash скриптов

Данный скрипт выводит события/сообщения в цвете.

## Использование

Для начала необходимость добавить следующий код в требуемый скрипт:

```
# Подключение библиотеки цветного вывода (URL проекта: http://git.sdamo.org/sdamo/bashlog)
BASHLOG="${HOME}/scripts/bashlog"
#BASHLOG=~/scripts/bashlog

if [[ -d "${BASHLOG}" ]]
then

    PATH=${PATH}:${BASHLOG}

fi
```

После чего для вывода событий следует использовать функцию **bashlog**:

```
bashlog INFO "Script running" TIME
```

где

- **INFO** Событие из списка (ERROR, INFO и др)
- **Script running** Сообщение
- **TIME** Вывод времени (По умолчанию время не отображается)