#### Parser Content
```Java
{
Name = vmware-esxi-str-app-notification-vsantraceurgent
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """vsantraceUrgent:""", """DOMTraceObjectServerAssocTerminateCb""" ]
  Fields = ${VMDLParsersTemplates.VMParserTemplates.Fields}[
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """({event_name}DOMTraceObjectServerAssocTerminateCb)"""
    ]


}
```