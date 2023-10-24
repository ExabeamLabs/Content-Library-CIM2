#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-key-cryptographicoperation
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Cryptographic operation.""", """Cryptographic Parameters:""", """Key Type:""", """Return Code:""" ]
  Fields = [
    """({event_name}Cryptographic operation)""",
    """Account Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Account Domain:""",
    """Account Domain:\s+({domain}[^\s]+)\s+Logon ID:""",
    """Logon ID:\s+({login_id}[^\s]+)\s+\w+""",
    """Operation:\s+({operation}[^:]+?)\.\s+Return Code"""
  ]


}
```