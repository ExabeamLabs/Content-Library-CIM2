#### Parser Content
```Java
{
Name = exabeam-aa-json-app-notification-queue
  Vendor = Exabeam
  Product = Advanced Analytics 
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ Exabeam """, """"queue":""", """"meanTimeToClose":""", """exabeam-soar-server"""]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) ({host}[\w.\-]+) ({app}Exabeam) """,
    """"event_name":"({event_name}[^"]+)""",
# incidentId is removed
    """"name":"({name}[^"]+)""",
    """"status":"({result}[^"]+)""",
# statusValue is removed
    """"priority":"({priority}[^"]+)""",
# incidentType is removed
# queue is removed
# assignee is removed
    """"createdAt":({time}\d+)""",
# createdBy is removed
# startedDate is removed
# endedDate is removed
# updatedAt is removed
# updatedBy is removed
    """"description":"({description}[^"]+)""",
    """"source":"({log_source}[^"]+)""",
# dwellTime is removed
# meanTimeToClose is removed
# isDeleted is removed
  ]
  ParserVersion = "v1.0.0"


}
```