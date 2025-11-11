#### Parser Content
```Java
{
Name = microsoft-o365-cef-alert-trigger-success-spoofmail
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""destinationServiceName =Office 365""",""""EventType":"SpoofMail""",""""Direction":"Inbound"""","""CEF:""" ]
  Fields = [
    """suser=(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+="""
    """"Date":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""""
	  """msg=({additional_info}[^$]+?)\s\w+=""",
	  """"SenderIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
	  """"Action":"({operation}[^"]+)""",
	  """"SpoofedSender":"({external_domain}[^"]+)"""",
	""""TrueSender":"({email_domain}[a-zA-z0-9.\-_]+\.[a-zA-Z]{2,})"""",
	""""EventType":"({alert_name}({alert_type}[^"]+))"""",
	""""Direction":"({direction}[^"]+)""",
 ]
 

}
```