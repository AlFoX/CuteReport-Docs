# ModelDataset

ModelDataset is designed to print model's data (inherited from QAbstractItemModel) from an application. Forprinting data some steps are necessary:

* CreateModelDataset inyour report;
* In the field "Model name"type in any name for your model. If there are some they should be different;
* For thereport testing you can fill test model with the data using any number of columns and rows;

All set. For printing your report you have to pass your model address (as longlong) to the report using report parameters.

For example:

```cpp
CuteReport::ReportCore * cuteReport =  new CuteReport::ReportCore();

    // load report
    QString err;
    CuteReport::ReportInterface * reportObject = cuteReport->loadReport("file:test.qtrp", &err);

    // if error, exist with message
    if (!reportObject) {
        QMessageBox::critical(this, "loadReport", err);
        return;
    }

    // making of the test model
    QStringList list;
    list << "11111" << "2222" << "333" << "44" << "5";

    model = new QStringListModel();
    model->setStringList(list);

    // Warning!!! Link tothe modelis passing as longlong
    // Set model name the same you have set in the ModelDataset before
    reportObject->setVariableValue("model1",qlonglong(model));


    // making reports preview window
    CuteReport::ReportPreview * preview = new CuteReport::ReportPreview(cuteReport);
    if (reportObject) {
        // set core and set preloaded report
        preview->setReportCore(cuteReport);
        preview->connectReport(reportObject);
        // report processing
        preview->run();

        //Preview window show
        preview->show();
    }
```

While rendering the datamodel will be cloned, since QAbstractItemModel is not thread safe.
