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
    """(MAIL FROM):<({src_email_address}.+?@([^@]+?))>""", #dl fields are removed
    """"message":".*?\\t\d+\\t({session_id}\d+)\\t.*?\\t\\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\"\\t\\"(\w+):""", #dl field removed
    """(RCPT TO):<({dest_email_address}.+?@([^@]+?))>""", #dl fields are removed
    """(?:MAIL FROM|RCPT TO):<({email_address}.+?)>""",
  ]


}
```