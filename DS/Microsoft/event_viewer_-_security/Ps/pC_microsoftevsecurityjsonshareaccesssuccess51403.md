#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-share-access-success-5140-3
    Vendor = Microsoft
    Product = "Event Viewer - Security"
    ParserVersion = v1.0.0
    TimeFormat = "yyyy-dd-MM'T'HH:mm:ss.SSSZ"
    Conditions = ["""A network share object was accessed""", """"SubjectUserName":""", """"event_id":"5140""",""""Microsoft-Windows-Security-Auditing"""",""""ShareName":""""]
    Fields = [
      """({event_name}A network share object was accessed)""",
      """"created":"({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.\d{3}Z)"""",
      """({event_code}5140)""",
      """"SubjectLogonId":"({login_id}[^"]+)"""",
      """"AccessList":"({access}[^"]+)"""",
      """"ShareLocalPath":"[\\?]*(({share_path}(({d_parent}.+?)\\)?(|({d_name}[^\\]+?)))\\?)"""",
      """"SubjectUserName":"({user}[\w\.\-]{1,40}\$?)"""",
      """"SubjectDomainName":"({domain}[^"]+)"""",
      """"IpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """({access}Read)""",
      """"ShareName":"([\\*]+)?({share_name}[^"]+)"""",
      """"outcome":"({result}\w+)"""",
      """"host":"({host}[\w.\-]+)"""",
      """Logon ID:\s({login_id}[^\s]+)""",
      """"IpPort":"({src_port}\d+)"""",
      """"SubjectUserSid":"({user_sid}[^"]+)"""",
      """"action":"({operation}[^"]+)""",
      """Source Port(=|:)\s*(\\t)*({src_port}\d+)"""
    ]
    DupFields=[ "host->dest_host" ]


}
```