# Какая проблема есть?

**Закупщики** всех уровней ежедневно сталкиваются с поиском ответа на вопрос: кого пригласить участвовать в тендере? Кому отправить запрос на получение коммерческого предложения? Под «Кого» и «Кому» имеются ввиду компании (потенциальные контрагенты) профиль работы которых и регион работы которых соответствует текущей потребности нашей организации. Каждый Закупщик ведёт свою собственную базу в своём формате. Также ведётся база контрагентов в Excel, содержащая часть данных. С аналогичной проблемой сталкиваются и сотрудники дочерних компаний. Кроме того, стоит проблема актуальности данных. Имеющиеся контактные данные устаревают и требуют периодического обновления.

# Диаграмма от Зины

```puml
@startuml
start

:Получение заявки на оплату;
if (Необходимо провести дополнительные проверки?) then (да)
  :Проведение дополнительных проверок;
else (нет)
endif

:Проверка заявки на соответствие правилам компании;
if (Заявка отклонена?) then (да)
  :Отправка уведомления об отклонении заявки;
else (нет)
  :Направление заявки на согласование;
endif

if (Требуется дополнительное согласование?) then (да)
  :Проведение дополнительного согласования;
else (нет)
  :Отправка заявки на оплату в бухгалтерию;
endif

:Проведение оплаты;
if (Оплата не прошла?) then (да)
  :Отправка уведомления об ошибке оплаты;
else (нет)
  :Отправка уведомления о проведении оплаты;
endif

stop
@enduml
```

Диаграмма отображает последовательность шагов в процессе согласования заявки на оплату, начиная с получения заявки на оплату и заканчивая отправкой уведомления о проведении оплаты. Если заявка не соответствует правилам компании, она может быть отклонена и отправлена на доработку. Если нужно провести дополнительные проверки или согласование, они также могут быть проведены в процессе согласования. В конечном итоге заявка отправляется на оплату в бухгалтерию, и если оплата прошла успешно, отправляется уведомление о проведении оплаты. Если же возникла ошибка при оплате, отправляется уведомление об ошибке оплаты.