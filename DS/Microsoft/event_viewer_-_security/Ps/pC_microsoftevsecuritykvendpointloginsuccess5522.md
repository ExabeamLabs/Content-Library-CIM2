#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-success-552-2
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """EventCode=552""", """The session cookies were successfully deleted""", """SourceName =AD FS""" ]
  Fields = [
    """({event_name}The session cookies were successfully deleted using the OAuth logout path.)""",
	  """({time}\d\d\/\d\d\/\d\d\d\d\s*\d\d:\d\d:\d\d\s*((?i)AM|PM))\s*LogName =""",
    """ComputerName =({host}[^\s]+)\s*User=""",
    """({event_code}552)""",
    """User=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Sid=""",
	  """Sid=({user_sid}[^\s]+)\sSidType=""",
	  """RecordNumber=({event_id}\d+)\s*"""
  ]
  ParserVersion = "v1.0.0"


}
```