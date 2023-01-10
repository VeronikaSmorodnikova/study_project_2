# study_project_2
 Данная работа посвящена анализу набора данных онлайн-школы.
 
## Содержание работы:
 1. Подготовка данных
 2. EDA
 3. Анализ аудитории и особенности прохождения курсов:
    1. Анализ завершаемости экзаменов
    2. Анализ регистрации на курсы
    3. Когортный анализ курсов
    4. Сегментация аудитории (RFM анализ)
  
## Описание файлов:
**1. test— датасет содержит информацию об оценках в тесте. Каждый предмет в семестре включает ряд тестов с оценками, за которыми следует заключительный экзамен.**

code_module — идентификационный код предмета.

code_presentation — семестр (Идентификационный код).

id_assessment — тест (Идентификационный номер ассессмента).

assessment_type — тип теста. Существуют три типа оценивания: оценка преподавателя (TMA), компьютерная оценка (СМА), экзамен по курсу (Exam).

date — информация об окончательной дате сдачи теста. Рассчитывается как количество дней с момента начала семестра. Дата начала семестра имеет номер 0 (ноль).

weight — вес теста в % в оценке за курс. Обычно экзамены рассматриваются отдельно и имеют вес 100%; сумма всех остальных оценок составляет 100%.

**2. courses — датасет содержит список предметов по семестрам.**
code_module — предмет (идентификационный код).

code_presentation — семестр (идентификационный код).

module_presentation_length — продолжительность семестра в днях.

**3. assessment — датасет содержит результаты тестов студентов. Если учащийся не отправляет работу на оценку, результат не записывается в таблицу.**
id_assessment — тест (идентификационный номер).

id_student — идентификационный номер студента.

date_submitted — дата сдачи теста студентом, измеряемая как количество дней с начала семестра.

is_banked — факт перезачета теста с прошлого семестра (иногда курсы перезачитывают студентам, вернувшимся из академического отпуска).

score — оценка учащегося в этом тесте. Диапазон составляет от 0 до 100. Оценка ниже 40 неудачная/неуспешная сдача теста.

**4. registration — датасет содержит информацию о времени, когда студент зарегистрировался для прохождения курса в семестре.**
code_module — предмет (идентификационный код).

code_presentation — семестр (идентификационный код)

id_student — идентификационный номер студента.

date_registration — дата регистрации студента. Это количество дней, измеренное от начала семестра (например, отрицательное значение -30 означает, что студент зарегистрировался на прохождение курса за 30 дней до его начала).

date_unregistration — дата отмены регистрации студента с предмета. У студентов, окончивших курс, это поле остается пустым.
