ModelDataset
-----
Предназначен для вывода данных модели (наследник QAbstractItemModel) из приложения в отчет.
Для вывода данных модели необходимо проделать несколько шагов:
* В вашем отчете создать ModelDataset
* В поле "Имя модели" указать любое имя для своей модели, если в отчете несколько таких dataset'ов, то имена должны отличатся.
* Для тестирования отчета можно заполнить тестовую модель данными. В ней можно создать любое кол-во колонок и строк.

Отчет готов, теперь для его просмотра, необходимо, в вашем приложении передать ссылку(в виде longlong) на существующую модель в параметр отчета.

Для примера
```cpp
CuteReport::ReportCore * cuteReport =  new CuteReport::ReportCore();

    //Загружаем отчет
    QString err;
    CuteReport::ReportInterface * reportObject = cuteReport->loadReport("file:test.qtrp", &err);

    // Если не удалось загрузить, то выходим с ошибков
    if (!reportObject) {
        QMessageBox::critical(this, "loadReport", err);
        return;
    }

	// Создание тестовой модели
    QStringList list;
    list << "11111" << "2222" << "333" << "44" << "5";

    model = new QStringListModel();
    model->setStringList(list);

	// ВАЖНО!!! Ссылка на модель в отчет передается в переменную отчета как long
	// Имя переменной указать то, какое имя указали в ModelDataset отчета
    reportObject->setVariableValue("model1",qlonglong(model));


    // Создаем окно просмотра отчета
    CuteReport::ReportPreview * preview = new CuteReport::ReportPreview(cuteReport);
    if (reportObject) {
        // Указваем ядро и указываем загруженный отчет
        preview->setReportCore(cuteReport);
        preview->connectReport(reportObject);
        // Обрабатываем отчет
        preview->run();

        // Показываем окно просмотра
        preview->show();
    }
```

При генерации отчета модель с данными клонируется, т.к. QAbstractItemModel не потокобезопасная.
