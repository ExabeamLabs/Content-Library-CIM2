#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-rdp-traffic-success-4778-1"
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """EventCategory=""", """EventID=4778""", """Microsoft-Windows-Security-Auditing""" ]
    Fields = [
      """Description=({event_name}[^\.]*).""",
      """({event_code}4778)""",
      """WindowsVersion=({os_version}.+?)\s*\w+=""",
      """({time}\d{1,4}-\d{1,2}-\d{1,2} \d{1,2}:\d{1,2}:\d{1,2})\s""",
      """User=(null|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\w+=""",
      """Client Address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
      """Client Name =({src_host}[^\s]*)\s"""
      """Account Name =({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s"""
      """Message=({additional_info}[^\.]*)."""
      """Account Domain=({domain}[^\s]*)\s"""
      """Logon ID=({login_id}[^\s]*)\s"""
      """ComputerName =({host}[^\s]*)\s""",
      """EventType=({result}.+?)\s*\w+=""",
      """Key\[0\]=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s""",
      """Key\[5\]=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """Key\[4\]=({host}[^\s]*)\s""",
      """Key\[2\]=({login_id}[^\s]*)\s""",
    ]
    ParserVersion = "v1.0.0"
  

}
```