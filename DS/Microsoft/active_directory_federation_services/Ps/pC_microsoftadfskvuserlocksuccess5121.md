#### Parser Content
```Java
{
Name = microsoft-adfs-kv-user-lock-success-512-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Active Directory Federation Services
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """EventCode=512""", """The account for the following user is locked out""", """SourceName =AD FS""" ]
  Fields = [
    """({event_name}The account for the following user is locked out.)""",
	  """({time}\d\d\/\d\d\/\d\d\d\d\s*\d\d:\d\d:\d\d\s*((?i)AM|PM))\s*LogName =""",
    """ComputerName =({host}[^\s]+)\s*User=""",
    """({event_code}512)""",
    """User=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Sid=""",
	  """Sid=({user_sid}[^\s]+)\sSidType=""",
	  """RecordNumber=({event_id}\d+)\s*""",
    """Client IP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """User:\s*(({domain}[^\\]+)[\\\/]*)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Client IP:"""
  ]


}
```