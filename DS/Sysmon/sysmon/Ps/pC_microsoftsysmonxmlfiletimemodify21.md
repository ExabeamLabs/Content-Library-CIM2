#### Parser Content
```Java
{
Name = microsoft-sysmon-xml-file-time-modify-2-1
  Product = Sysmon
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>2</EventID>""", """<Provider Name""","""'Microsoft-Windows-Sysmon'""" ]
  DupFields = [ "host->dest_host" ]


}
```