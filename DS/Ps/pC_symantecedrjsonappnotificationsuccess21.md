#### Parser Content
```Java
{
Name = symantec-edr-json-app-notification-success-2-1
  ParserVersion = v1.0.0
  Conditions = [ """"destinationServiceName":"Symantec"""", """"event_data_type":"sep"""",""""type_id":2""" ]
  Fields = ${DLSymantecParserTemplates.symantec-system-info-template.Fields}[
    """"message":"({additional_info}.+?)","\w+":"""
  ]


}
```