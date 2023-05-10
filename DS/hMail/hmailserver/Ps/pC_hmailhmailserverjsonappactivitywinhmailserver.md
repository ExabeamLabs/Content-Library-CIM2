#### Parser Content
```Java
{
Name = hmail-hmailserver-json-app-activity-winhmailserver
  ParserVersion = "v1.0.0"
  Vendor = hMail
  Product = hMailServer
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"log_type":"win_hmailserver"""" ]
  Fields = [
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"host":\{"name":"({host}[^"]+)""",
    """"log_type":"({event_category}[^"]+)""",
    """"message":".*?\\t\d+\\t({session_id}\d+)\\t.*?\\t\\"({src_ip}[a-fA-F\d.:]+)\\"\\t\\"(\w+):""", #dl field removed
    """(MAIL FROM):<({email_address}.+?@([^@]+?))>""", #dl fields are removed
    """(RCPT TO):<({dest_email_address}.+?@([^@]+?))>""", #dl fields are removed
    """(?:MAIL FROM|RCPT TO):<({email_address}.+?)>""",
  ]


}
```