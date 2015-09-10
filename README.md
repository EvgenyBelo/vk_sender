# vk_spam
Скрипт для рассылки личных сообщений участникам сообщества/группы. Python 2.7

# Команды:
 
- help - показать справку
- exit - закрыть
- auth - авторизоваться в ВК
- deauth - завершить работу текущим авторизованным пользователем
- user - показать пользователя авторизованного в данный момент
- task - назначить новую задачу
- start - начать рассылку

# Порядок работы:
- зайти в ВК с помощью команды "auth"
- назначить новую задачу командой "task"
- ввести "start"
        
# Важные моменты:
- Нужно вводить id группы именно в числовом виде, а не в виде домена. Узнать его можно по ссылке в браузере,
например https://vk.com/club123456, где 123456 - id группы. Если у группы есть домен, например https://vk.com/verycoolgroup,
то id группы можно узнать наведя указатель мыши на любой статический объект, например на картинку-обложку группы,
на ней будет ссылка вида https://vk.com/photo-123456_358964541, где 123456 - id группы
- Интервал между отправками сообщений - переменный, рассчитывается он как "interval value" плюс/минус "interval gap",
т.о. при значениях 60 и 10 интервал будет случайно выбираться из диапазона 50-70 секунд
- Выбирайте интервал осторожно. Скрипт не рассчитан на обход капчи антигейтом. Возможно, допишу в дальнейшем, или,
если желаете, форкните и сделайте сами. Оптимальный интервал - не меньше минуты
- При назначении задачи будет спрошен файл с текстом сообщения. Нужно указать полное имя файла, включая расширение,
например message.txt
- Текст в файле должен быть закодирован в UTF-8. Это важно! Иначе вместо кириллических букв будет ерунда. Вам будет
показана превьюшка сообщения. Пожалуйста, убедитесь что вы видите нормальные русские буквы, иначе получателям отправится
бессвязный набор случайных символов

 И ещё:
- Каждому получателю отправляется уникальное сообщение - чередуются русские символы с английскими
- Когда задача назначена, рассылку можно приостанавливать просто закрыв окно консоли. Когда необходимо запускаете
скрипт заново и вводите "start". Рассылка начнется с того места где была остановлена
- Если по каким-либо причинам сообщение не будет отправлено, запись об этом будет записана в лог (log.txt)
