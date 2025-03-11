#### Parser Content
```Java
{
Name = microsoft-azuremon-json-database-activity-success-automatictuningsettingssnapshotevent
  Product = Azure Monitor
  ParserVersion = v1.0.0
  Conditions = [ """"resourceId":""", """"category":"AutomaticTuning"""", """"operationName":"AutomaticTuningSettingsSnapshotEvent"""" ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-db-for-mysql.Fields} [
	  """"StartTime":"({time}\d\d\d\d\-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  ]


}
```