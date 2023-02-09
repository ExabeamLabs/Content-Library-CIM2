#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-trustedlogonprocessregister
    Vendor = Microsoft
    Product = Event Viewer - System
    ParserVersion = v1.0.0
    TimeFormat = "MMM dd HH:mm:ss yyyy"
    Conditions = [ """Microsoft-Windows-Security-Auditing""", """A trusted logon process has been registered""" ]
    Fields = [
      """DetectTime=({time}\d\d\d\d-\d{1,2}-\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2})""",
      """({time}\w{3}\s\d{2}\s\d{2}:\d{2}:\d{2}\s\d{4})""",
      """({event_code}4611)""",
      """(Information|Audit Success|Success Audit|Audit Failure|Failure Audit)(\s+|\s*,\s*)({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[^\s,]+)))""",
      """(::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[^\/\s]+)))\/Microsoft-Windows-Security-Auditing""",
      """__li_source_path="(::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[^"]+)))"""",
      """Computer(Name)?["\s]*(:|=)\s*"?(::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[^$]+?)))("|\s)""",
      """Security ID:\s+({user_sid}.+?)\s+Account Name:\s+(?=\w)({user}.+?)\s+Account Domain:\s+(?=\w)({domain}.+?)\s+Logon ID""",
      """Logon ID:\s+({login_id}.+?)\s+Logon Process Name:\s+({process_name}[^,\s]+)""",
      """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|({dest_host}[\w\-.]+)))""",
      """Subject:Security ID=({user_sid}\S+)""",
      """Subject:Account Name =({user}[^\s]+)\sSubject:""",
      """Subject:Account Domain=({domain}[^\s]+)\sSubject:""",
      """Subject:Logon ID=({login_id}[^\s]+)\s""",
      """Logon Process Name =({process_name}\S+)"""
    ]


}
```