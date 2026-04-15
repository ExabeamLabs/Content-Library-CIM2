#### Parser Content
```Java
{
Name = microsoft-evapp-xml-endpoint-notification-3005
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = Event Viewer - Application
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss"]
  Conditions = [ """<Channel>Application</Channel>""", """<Provider Name =""",  """<Event xmlns=""" , """>Event code: 3005""" ]
  Fields = [
    """<TimeCreated SystemTime="({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2})""",
    """<Computer>({dest_host}({host}[\w_\-\.]+))</Computer>""",
    """Provider Name ="({app}[^"]+)""",
    """<EventID[^>]*>({event_code}\d+)</EventID>""",
    """<Data>({event_id}[a-z0-9\-]{36})</Data>""",
    """Exception message:\s+({failure_reason}[^	]+?)(\s+at\s+System\.|$)""",
    """Account name:\s*(({domain}[^\\]+)\\*)?(\s|\\[rnt])*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s|\\[rnt])+Exception information:""",
    """Process ID:\s({process_id}\d+)""",
    """Process name:\s+({process_name}[^=]+?)(\s|\\[rnt])+Account name:""",
    """Machine name:\s+({device_name}[\w\.-]+)""",
    """User host address:\s+({src_ip}(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?))""",
    """Request URL:\s+({url}https?://[^\s]+)""",
    """Request path:\s+({uri_path}[^\s]+)""",
    """Application Path:\s+({file_path}[^\s]+?)(\s+Machine|\s*$)"""
    """<Channel>({channel}[^<]+)<\/Channel>"""    
  ]


}
```