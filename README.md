# Lesson4

## Практическая работа №4

### Задание 1. 

  Требуется создать экран музыкального плеера с использованием «binding» для горизонтальной и портретной ориентации.
  Модуль app

В файл разметки «activity_main» требуется добавить несколько элементов графического интерфейса («button», «textView» и т.д.) и установить соответствующий идентификатор.
Включить viewBinding в build.gradle.kts

![image](https://github.com/user-attachments/assets/eac181fe-59e7-41ce-843b-57b2d88af15e)

### Задание 2. 

Создать новый модуль. В меню «File | New | New Module | Phone & Tablet Module | Empty Views Activity». Имя модуля «thread». На экране требуется разместить элементы «Button» и «TextView». Инициализацию графических компонентов осуществить с помощью «Binding». Посчитать в фоновом потоке среднее количество пар в день за период одного месяца. Общее количество пар и учебных дней вводятся в главном экране. Отобразить результат в «TextView».
Создадать текст и кнопку
Создадать инициализацию через binding 
Добавить еще два поля: дни и пары
Расчет и вывод на экран по нажатию кнопки. 

![image](https://github.com/user-attachments/assets/007f198e-ce78-4fb1-86db-95cfb48cd169)

После многочисленных нажатий на кнопку приложение сломалось

![image](https://github.com/user-attachments/assets/9052a151-182b-485f-a85f-4d70ec7122d3)

### Задание 3
Создать новый модуль. В меню «File | New | New Module | Phone & Tablet Module | Empty Views Activity». Имя модуля: «data_thread».
Требуется определить в какой последовательности происходит запуск процессов. 
Сначала идет задержка в 2 секунды, потом выводится runn1, затем идет задержка в 1 секунду и одновременно выводится runn2 и запускается задержка в 2000 миллисекунд для вывода runn3
Изучите методы «runOnUiThread», «postDelayed», «post». 
Данные методы позволяют взаимодействовать с пользовательским интерфейсом (обновлять элементы экрана, изменять видимость элементов и прочее) из другого потока, например, рабочего потока или обработчика сообщений.
Метод runOnUiThread(Runnable action) предназначен для выполнения операций в главном потоке (UI thread) сразу же после вызова метода. Когда какой-то другой поток хочет изменить интерфейс, он вызывает этот метод, передавая объект Runnable, который представляет собой блок кода, предназначенный для исполнения в UI thread.
Метод post(Runnable action) используется для отправки задачи на исполнение в очередь сообщений главного потока. Задача будет выполнена после того, как система завершит текущие задачи, находящиеся в очереди.
Метод postDelayed(Runnable action, long delayMillis) похож на метод post, однако добавляет задержку перед исполнением задачи. Задержка задаётся в миллисекундах. Таким образом, задание ставится в очередь сообщений UI thread, но не сразу, а спустя указанное время.

В «TextViwe» описать в чём различия между элементами и последовательность запуска. У элемента «TextView» имеется возможность установки значений строк: android:maxLines="10" android:lines="10"

![image](https://github.com/user-attachments/assets/3945646e-30fd-4cfc-8e47-07cec544f91a)

### Задание 4
Создать новый модуль. В меню «File | New | New Module | Phone & Tablet Module | Empty Views Activity». Имя модуля: «looper». В main_activity.xml требуется добавить «button» и реализовать обработку нажатия.
Реализуйте пример, в котором вводится Ваш возраст и кем Вы работаете. Количество лет соответствует времени задержки. Результат вычисления осуществлять через Log.d.

![image](https://github.com/user-attachments/assets/39c904c0-36dd-4364-8729-57018261f433)

### Задание 5
Создать новый модуль. В меню «File | New | New Module | Phone & Tablet Module | Empty Views Activity». Имя модуля: «CryptoLoader».

Для реализации собственного загрузчика, требуется создание класса и переопределение методов «loadInBackground» и «onStartLoading». Имя класса MyLoader («New->JavaClass->…»):

![image](https://github.com/user-attachments/assets/1ce46e15-7ca0-41fb-b7eb-b7255b13bf50)

### Задание 6
 В созданном модуле требуется добавить элементы «EditText» и «Button». Пользователь вводит фразу в «EditText», далее она шифруется с помощью алгоритма AES и передается вместе с ключом в «Loader». В «Loader» происходит дешифровка фразы и последующая передача в «MainActivity». Дешифрованная фраза отображается с помощью «toast» или «snackBar».

![image](https://github.com/user-attachments/assets/0a25ccbf-c747-4b57-a5cf-e8f3cc815c01)

### Задание 7

Создать новый модуль. В меню «File | New | New Module | Phone & Tablet Module | Empty Views Activity». Имя модуля: «ServiceApp».
Создание сервиса

![image](https://github.com/user-attachments/assets/45287f97-6504-4f2f-8604-77ecfcfb21ba)

Т.к. сервис является компонентом приложения, требуется убедиться в существовании записи о сервисе в секции «application» манифест-файла

![image](https://github.com/user-attachments/assets/df97ae54-702e-461a-a2b3-ba2d232291ae)

### Задание 8

Требуется добавить функционал воспроизведения аудиофайла. В первую очередь необходимо добавить медиа файл (типа «.mp3» и т.д.) в ресурсы. В активности добавить две кнопки «button» для воспроизведения и остановки музыкальных композиций/композиции. Придумать собственный дизайн данного проигрывателя.

![image](https://github.com/user-attachments/assets/1e6e9f3c-01db-4401-aac5-60bc7535d64a)

![image](https://github.com/user-attachments/assets/8f448f20-29f4-4c80-9bf6-20ddfad5d1ab)

### Задание 9 

Создать новый модуль. В меню «File | New | New Module | Phone & Tablet Module | Empty Views Activity». Имя модуля: «WorkManager». Добавить в пример критерии запуска: напр. наличие интернета.

В файл build.gradle(Module …) в раздел dependencies требуется добавить библиотеку для работы с worker:

В модуле требуется создать класс UploadWorker с родительским классом Worker В MainActivity добавить вызов Worker: 

![image](https://github.com/user-attachments/assets/60726176-c991-4330-9014-fc1b8468ce19)

![image](https://github.com/user-attachments/assets/21341059-f52a-4cce-aba2-f2b6dc161c86)

