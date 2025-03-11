#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-logout-success-4779-2
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"EventID":4779""", """"ClientName":"""", """"SessionName":"""" ]
  Fields = [
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """({event_name}A session was disconnected from a Window Station)""",
    """"Hostname":"({host}[\w\-.]+)"""",
    """({event_code}4779)""",
    """"AccountName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"AccountDomain":"({domain}[^"\\]+)"""",
    """"LogonID":"({login_id}[^"\\]+)"""",
    """"SeverityValue":({severity}[^,]+)""",
    """"ClientName":"({dest_host}[\w\-.]+)"""",
    """"ClientAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"SessionName":"({session_name}[^"]+)"""",
    """"SourceName":"({provider_name}[^"]+)"""",
    """"ProcessID":({process_id}\d+),""",
    """"Category":"({category}[^"]+)"""",
  ]
  ParserVersion = "v1.0.0"


}
```