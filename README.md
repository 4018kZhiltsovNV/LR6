# Лабораторная работа №6
Для начала необходимо создать копию репозитория в личном хранилище

![1](https://user-images.githubusercontent.com/94634803/142620924-7ddb40f4-f6fa-455b-a730-ce331cdf1382.png)

Далее используя команды __git config --global user.name <username>__ и __git config --global user.email <email>__ для того, чтобы ввести свои данные __GitHub__
  
![2](https://user-images.githubusercontent.com/94634803/142621055-a258f60a-184a-4a28-b7e9-db11865a10ed.png)
  
Клонируем удаленный репозиторий, используя команду __git clone__ 
  
![3](https://user-images.githubusercontent.com/94634803/142621202-ca44e181-fd8e-40c5-9476-03be2aa55437.png)
  
Добавим файл через интерфейс GitHub. Далее переходим в директорию __LR6__ командой __cd LR6/__ для работы с файлами
  
![4](https://user-images.githubusercontent.com/94634803/142621293-f3444d5b-c424-4752-aed7-4f8bdc2a457d.png)
  
Подтянем изменения из веб-интерфейса GitHub для клиента Git. Для этого используем команду __git pull__
  
![5](https://user-images.githubusercontent.com/94634803/142621457-a6125431-3b9e-4cc5-9de7-63407444e7da.png)
  
Посмотрим коммиты ветки master, используя команду __git log__
  
![6](https://user-images.githubusercontent.com/94634803/142621529-48d98ebe-ec5f-43de-a18d-22aea0566a23.jpg)
  
Просмотрим существующие ветки в текщем репозитории командой __git branch__. Перейдем в ветку branch1 командой __git checkout branch1__
  
![7](https://user-images.githubusercontent.com/94634803/142621595-e99417f4-7caa-4d86-a0da-7e1f0ca6ab34.png)
  
Посмотрим коммиты ветки branch1 командой __git log__
  
![8](https://user-images.githubusercontent.com/94634803/142621680-dfee5c36-312e-4a47-bd69-272d3dae3a5c.png)
  
Рассмотрим подробно коммиты командой __git log -p__
  
![9](https://user-images.githubusercontent.com/94634803/142621730-b66ee7a7-7165-433e-8241-693555a5aa2e.png)
  
Вернемся в ветку master и выполним слияние в ветку master. Слияние производить командой __git merge branch1__
  
![10](https://user-images.githubusercontent.com/94634803/142621889-3caff9f4-dca6-424a-9bac-3f6d0ed59306.png)
  
Произошел конфликт. Скорее всего из-за того, что файл mergefile.txt не отслеживается. Используем команду __git status__. Теория оказалась верна. Добавим файл для отслеживания командой __git add__ mergefile.txt. Проверим еще раз, отслеживается ли файл. Супер, осталось только оставить коммит __git commit -m "Branches"__

Удалим побочную ветку __git branch1__
  
![11](https://user-images.githubusercontent.com/94634803/142622180-5230adc7-e02a-4e3d-bdb8-e4c76171fe40.png)

Создадим изменения и комментарии для них. Создавать будем текстовые файлы прямо в терминале. Для создания текстовика используем команду echo hello > change1.txt, зафиксируем его __git add__ change1.txt. Оставим комментарий __git commit -m "Change1.txt"__. Повторем все то же самое еще раз, только название указываем другое - __change2.txt__
  
![12](https://user-images.githubusercontent.com/94634803/142622373-eac095c6-dd13-4b7f-a450-48e62aea129a.png)

Посмотрим комментарии
  
![13](https://user-images.githubusercontent.com/94634803/142622454-81b8e928-cb12-4feb-ac5d-67cf3f732920.png)

Все сработало, отлично. Теперь сделаем хард откат коммита. Вводим команду git reset --hard HEAD~1
  
![14](https://user-images.githubusercontent.com/94634803/142622642-0712dbe5-1be2-4c91-86c1-24fa658d27bb.png)
  
Создадим ветку для отчета и перейдем в нее при помощи команды __git branch report__
  
![15](https://user-images.githubusercontent.com/94634803/142622701-71db1664-b3ed-4f93-9b7a-66f1d9af2095.png)

Отчет, написанный в программе VS Code перемещаем в каталог LR6 и не забываем про команды __git add__ и __git commit__

Получим итоговую историю операций __git log__
  
![16](https://user-images.githubusercontent.com/94634803/142622783-52a54561-b1e4-4072-87fa-9d5ef174fe3d.png)

 После редактирования отчета, его нужно будет сохранить и выполнить команды __git add__ и __git commit__.

Папку со скриншотами просто переместим в директорию проекта.

В конце работы необходимо будет отправить все локальные изменения в сетевое хранилище __GitHub__ командой  __git push__
