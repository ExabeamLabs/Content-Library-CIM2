#### Parser Content
```Java
{
Name = microsoft-sysmon-xml-process-close-5
  ParserVersion = v1.0.0
  Product = Sysmon
  Conditions = [ """<EventID>5</EventID>""", """<Provider Name""","""'Microsoft-Windows-Sysmon'""" ]
  DupFields = [ "host->dest_host" ]


}
```