#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-endpoint-4624
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = [ """EventID': 4624""", """destinationServiceName =""" ]
  DupFields = [ "dest_user->user","dest_domain->domain","host->dest_host" ]


}
```