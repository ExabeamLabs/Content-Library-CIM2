#### Parser Content
```Java
{
Name = microsoft-exchange-csv-app-authentication-success-server
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """Exchange Server""", """,authenticated""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)(,[^,]*){3},({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+),[^,]*,(({domain}[^\\\s\@]+)\\)?(({email_address}[^\s\@]+\@({email_domain}[^\s]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),({event_name}authenticated)\s*""",
    """({app}Exchange Server)"""
  ]
  ParserVersion = "v1.0.0"


}
```