#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-success-5442
    Vendor = Microsoft
    Product = Event Viewer - Security
    ParserVersion = "v1.0.0"
    Conditions = [ """EventCode=5442""", """SourceName =Microsoft Windows security auditing.""", """TaskCategory=""" ]
    Fields = ${WindowsParsersTemplates.windows-events.Fields}[
      """ComputerName =({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+))""",
      """Workstation Name\s*:\s*(-|({src_host_windows}[^\s]+))\s+Logon GUID:""",
      """Workstation Name\s*:\s*(-|({src_host}[\w\-\.]+))\s+Logon GUID:.*?Source Network Address:\s*-\s+""",
      """Computer(Name)?="?({host}[\w\-.]+)"?"""
      """LogName =({log_name}[^\s]+)"""
      """RecordNumber=({event_id}\d+)"""
      """TaskCategory=({operation}[^=]+?)\s*(\w+=|$)"""
      """SourceName =({service_name}.+?)(\.\s+\w+=|\s*$)"""
      """Subject:.+?Security ID:\s*(|-|({user_sid}.+?))\s*Account Name:\s*(|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:\s*(|-|({domain}.+?))\s*Logon ID:\s*(|-|({login_id}\S+))\s"""	
    ]
  
windows-events = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)('|")""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task_name}[^<]+)"""
    """<Level>({run_level}[^<]+)<"""
  
}
```