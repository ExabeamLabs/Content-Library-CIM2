#### Parser Content
```Java
{
Name = microsoft-exchange-kv-app-authentication-success-exserver
  Conditions = [ """Imap4""", """Exchange Server""", """,authenticate,""", """"R=OK""" ]
  Fields = ${DLMicrosoftParsersTemplates.exchange-server-authentication.Fields}[
    """"R=({result}OK)""",
  ]
  ParserVersion = "v1.0.0"

exchange-server-authentication = {
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [ """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)(,[^,]*){2},(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({dest_port}\d+)|\[?({=dest_ip}[\da-fA-F.:]+)\]?:({=dest_port}\d+)),(\[?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\]?:({src_port}\d+)|\[?({=src_ip}[\da-fA-F.:]+)\]?:({=src_port}\d+)),({user}[^,]+)(,[^,]*){3},({event_name}[^,]+),"""
    """({app}Exchange Server)""",
    """Msg="({additional_info}[^"]+)""",
  
}
```