#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-rdp-traffic-success-4778"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["epoch_sec", "yyyy-MM-dd HH:mm:ss"]
  Conditions = [
    """"A session was reconnected to a Window Station"""
    """"EventID"""
    """:4778"""
    """"ClientName"""
    """"Category"""
    """Logoff Events""" 
  ]
  Fields = [
    """"EventTime":({time}\d{10})"""
    """"EventTime\\?":\s*\\?"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""
    """"Hostname\\?":\\?"({host}[\w.-]+?)\\?""""
    """"EventID\\?":({event_code}\d+)"""
    """({event_name}A session was reconnected to a Window Station)"""
    """Client Name:(\\r|\\t|\\n)*({src_host}[\w\-\.]+)(\\r|\\t|\\n)*"""
    """"AccountName\\?":\\?"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\?""""
    """"AccountDomain\\?":\\?"({domain}[^"]+?)\\?""""
    """"LogonID\\?":\\?"({login_id}[^"]+?)\\?""""
    """"ClientName\\?":\\?"({src_host}[^"]+?)\\?""""
    """"ClientAddress\\?":\\?"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """Client Address:(\\r|\\n|\\t)*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  ]
  DupFields = [
    "host->dest_host"
  ]


}
```