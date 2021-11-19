# Лабораторная работа №6
Для начала необходимо создать копию репозитория в личном хранилище
![1](https://user-images.githubusercontent.com/94634803/142620924-7ddb40f4-f6fa-455b-a730-ce331cdf1382.png)
Далее используя команды git config --global user.name <username> и git config --global user.email <email> для того, чтобы ввести свои данные GitHub
![2](https://user-images.githubusercontent.com/94634803/142621055-a258f60a-184a-4a28-b7e9-db11865a10ed.png)
Клонируем удаленный репозиторий, используя команду git clone 
![3](https://user-images.githubusercontent.com/94634803/142621202-ca44e181-fd8e-40c5-9476-03be2aa55437.png)
Добавим файл через интерфейс GitHub. Далее переходим в директорию LR6 командой cd LR6/ для работы с файлами
![4](https://user-images.githubusercontent.com/94634803/142621293-f3444d5b-c424-4752-aed7-4f8bdc2a457d.png)
Подтянем изменения из веб-интерфейса GitHub для клиента Git. Для этого используем команду git pull
![5](https://user-images.githubusercontent.com/94634803/142621457-a6125431-3b9e-4cc5-9de7-63407444e7da.png)
Посмотрим коммиты ветки master, используя команду git log
![6](https://user-images.githubusercontent.com/94634803/142621529-48d98ebe-ec5f-43de-a18d-22aea0566a23.jpg)
Просмотрим существующие ветки в текщем репозитории командой git branch. Перейдем в ветку branch1 командой git checkout branch1
![7](https://user-images.githubusercontent.com/94634803/142621595-e99417f4-7caa-4d86-a0da-7e1f0ca6ab34.png)
Посмотрим коммиты ветки branch1 командой git log
![8](https://user-images.githubusercontent.com/94634803/142621680-dfee5c36-312e-4a47-bd69-272d3dae3a5c.png)
Рассмотрим подробно коммиты командой git log -p
![9](https://user-images.githubusercontent.com/94634803/142621730-b66ee7a7-7165-433e-8241-693555a5aa2e.png)
Вернемся в ветку master и выполним слияние в ветку master. Слияние производить командой git merge branch1.
![10](https://user-images.githubusercontent.com/94634803/142621889-3caff9f4-dca6-424a-9bac-3f6d0ed59306.png)
Произошел конфликт. Скорее всего из-за того, что файл mergefile.txt не отслеживается. Используем команду git status. Теория оказалась верна. Добавим файл для отслеживания командой git add mergefile.txt. Проверим еще раз, отслеживается ли файл. Супер, осталось только оставить коммит git commit -m "Branches"
