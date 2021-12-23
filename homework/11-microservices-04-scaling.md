
# Домашнее задание к занятию "11.04 Микросервисы: масштабирование"

Вы работаете в крупной компанию, которая строит систему на основе микросервисной архитектуры.
Вам как DevOps специалисту необходимо выдвинуть предложение по организации инфраструктуры, для разработки и эксплуатации.

## Задача 1: Кластеризация

Предложите решение для обеспечения развертывания, запуска и управления приложениями.
Решение может состоять из одного или нескольких программных продуктов и должно описывать способы и принципы их взаимодействия.

Решение должно соответствовать следующим требованиям:
- Поддержка контейнеров;
- Обеспечивать обнаружение сервисов и маршрутизацию запросов;
- Обеспечивать возможность горизонтального масштабирования;
- Обеспечивать возможность автоматического масштабирования;
- Обеспечивать явное разделение ресурсов доступных извне и внутри системы;
- Обеспечивать возможность конфигурировать приложения с помощью переменных среды, в том числе с возможностью безопасного хранения чувствительных данных таких как пароли, ключи доступа, ключи шифрования и т.п.

Обоснуйте свой выбор.

|Требование|Kubernetes|Nomad|Docker Swarm|
|-|---------|-----|-------------|
|Поддержка контейнеров|+|+|+|
|Обеспечивать обнаружение сервисов и маршрутизацию запросов|+|-|+|
|Обеспечивать возможность горизонтального масштабирования|+|+|+|
|Обеспечивать возможность автоматического масштабирования|+|+|-|
|Обеспечивать явное разделение ресурсов доступных извне и внутри системы|+|+|-|
|Обеспечивать возможность конфигурировать приложения с помощью переменных среды, в том числе с возможностью безопасного хранения чувствительных данных таких как пароли, ключи доступа, ключи шифрования и т.п|+|+|+|

Из выбранных мной систем больше всего подходит Kubernetes, если компания действительно крупная, то его сложность не будет являться минусом, тем более можно использовать одно из managed-решений.
Так же необходимые функции могут быть добавлены и в другие системы, путем интеграции со сторонним ПО. Но так как доля kubernetes и его managed-аналогов на рынке достаточно велика видимо нет никакого смысла использовать что-то другое.