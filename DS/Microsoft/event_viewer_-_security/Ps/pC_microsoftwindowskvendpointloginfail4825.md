#### Parser Content
```Java
{
Name = microsoft-windows-kv-endpoint-login-fail-4825
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "MM/dd/yyyy hh:mm:ss a"
    Conditions = ["""EventCode=4825""", """Microsoft Windows security auditing.""", """A user was denied the access to Remote Desktop."""]
    Fields = [
      """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(am|AM|pm|PM))""",
      """EventCode=({event_code}\d+)\s*""",
      """User Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Domain:\s+({domain}.+?)\s+Logon ID:\s+({login_id}[^\s]+)\s+""",
      """Client Address:\s+(::[\w]+:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """Message=({event_name}A user was denied the access to Remote Desktop).""",
      """ComputerName =({host}[\w.\-]+)"""
      """RecordNumber=({event_id}\w+)"""
      """LogName =({log_name}[^\s]+)"""
    ]
    ParserVersion = "v1.0.0"
  

}
```