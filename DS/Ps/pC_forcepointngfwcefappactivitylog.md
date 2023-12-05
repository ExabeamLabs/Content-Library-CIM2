#### Parser Content
```Java
{
Name = forcepoint-ngfw-cef-app-activity-log
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|FORCEPOINT|""", """|Log_Compress-SIDs|""" ]
  Fields = ${DLForcepointParsersTemplates.forcepoint-template.Fields} [
    ]
  DupFields = ["operation->event_name"]


}
```