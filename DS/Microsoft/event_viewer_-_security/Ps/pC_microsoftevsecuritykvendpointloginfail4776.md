#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-fail-4776
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0" 
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = ["""EventCode=4776""", """The computer attempted to validate the credentials""", """ComputerName =""", """Authentication Package"""]
  Fields =[
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d \w+)[^=]+?LogName =""",
    """({event_code}4776)""",
    """ComputerName =({host}[\w\-\.]+)""",
    """Message=({event_name}[^<=]+?)\s*<""",
    """The ({login_type_text}computer|domain)(\s\w+)? attempted to validate the credentials""",
    """Error Code:\s*({result_code}[^\s"]+)\s*"?""",
    """Source Workstation:\s*({src_host}[^\s\<]+)\s*(<14>)?""",
    """Logon Account:\s*(({user_upn}[^<:@]+@[^\.]+\.[^<:]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(<14>)?Source Workstation:""",
   ]
   DupFields = [
    "result_code->failure_code"
   ]


}
```