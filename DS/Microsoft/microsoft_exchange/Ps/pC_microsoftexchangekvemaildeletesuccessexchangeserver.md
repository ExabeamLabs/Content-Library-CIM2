#### Parser Content
```Java
{
Name = microsoft-exchange-kv-email-delete-success-exchangeserver
  Conditions = [ """Imap4""", """Exchange Server""", """,expunge,""", """R=OK""" ]
  ParserVersion = "v1.0.0"
  Fields = ${DLMicrosoftParsersTemplates.exchange-server-authentication.Fields}[
    """ActivityContextData="+({additional_info}[^"]+)""",
  ]
  DupFields = ["event_name->operation"]

exchange-server-authentication = {
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [ """(\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)(,[^,]*){2},(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({dest_port}\d+)|\[?({=dest_ip}[\da-fA-F.:]+)\]?:({=dest_port}\d+)),(\[?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\]?:({src_port}\d+)|\[?({=src_ip}[\da-fA-F.:]+)\]?:({=src_port}\d+)),({user}[\w\.\-\!\#\^\~]{1,40}\$?)(,[^,]*){3},({event_name}[^,]+),"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
    """({app}Exchange Server)""",
    """Msg="({additional_info}[^"]+)""",
  
}
```