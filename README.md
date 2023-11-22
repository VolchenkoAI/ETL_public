<h1>Построение ETL процесса</h1>

<h3>Описание задачи.</h3>
Разработать ETL процесс, получающий ежедневную выгрузку данных
(предоставляется за 3 дня), загружающий ее в хранилище данных и ежедневно
строящий отчет.

<h3>Выгрузка данных.</h3>
Ежедневно некие информационные системы выгружают три следующих
файла:
1. Список транзакций за текущий день. Формат – CSV.
2. Список терминалов полным срезом. Формат – XLSX.
3. Список паспортов, включенных в «черный список» - с накоплением с начала
месяца. Формат – XLSX.
Сведения о картах, счетах и клиентах хранятся в СУБД PostgreSQL.

<h3>Признаки мошеннических операций для построения отчета (FRAUD).</h3>
1. Совершение операции при просроченном или заблокированном паспорте.
2. Совершение операции при недействующем договоре.
3. Совершение операций в разных городах в течение одного часа.
