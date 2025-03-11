#### Parser Content
```Java
{
Name = microsoft-azuremon-json-app-activity-jupytersessionspecificidaction
  Product = Azure Monitor
  ParserVersion = v1.0.0
  ExtractionType = json
  Conditions = [ """"resourceId":""", """"category":"GatewayApiRequests"""", """"operationName":"JupyterSessionSpecificIdAction"""" ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-db-for-mysql.Fields} [
	""""StartTime":"({time}\d\d\d\d\-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  ]


}
```