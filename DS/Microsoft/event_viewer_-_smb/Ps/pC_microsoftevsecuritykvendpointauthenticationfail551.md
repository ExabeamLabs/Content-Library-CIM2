#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-authentication-fail-551
  Product = Event Viewer - SMB
  Conditions = [ """SMB Session Authentication Failure""", """Microsoft-Windows-SMBServer""", """ 551 """ ]
  ParserVersion = "v1.0.0"
  Fields = ${WindowsParsersTemplates.windows-events-share.Fields}[
    """({host}[\w\-\.]+)\s+None"""
  ]
  DupFields = [ "host->src_host" ]

windows-events-share = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss yyyy"]
  Fields = [
    """\s({time}[a-zA-Z]{3} \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
    """({time}\d{1,4}-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """\d+\s+({event_code}\d+)\s+Microsoft-Windows-SMB(Server|Client)"""
    """None\s+({event_name}[^\:]+?)\s+Client Name"""
    """Client Address(:|=)\s*(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """User Name:\s*(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Session ID"""
    """Session ID:\s*({session_id}[^\s]+)"""
    """Status:\s*({failure_reason}[^:.]+)\.\s+({failure_code}[^:]+?)\s+SPN"""
    """SPN:\s*({service_name}[^:]+)\s+SPN"""
    """Guidance:\s*({additional_info}[^:.,]+)"""
    """\s({dest_ip}((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({dest_port}\d+))?\s+[^\s]+\s+\-?\s*MSWinEventLog"""
    """({result}Fail|denied)"""
    """({log_name}MSWinEventLog)"""
  
}
```