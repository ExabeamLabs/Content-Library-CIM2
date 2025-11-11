#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-4768
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Kerberos Authentication Service""", """Microsoft-Windows-Security-Auditing""","""ServiceName:""", """TicketOptions:""", """4768""", """TicketEncryptionType:"""]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d{1,3}[+\-]+\d\d:\d\d""",
    """({host}[^\s]+)\s+Kerberos Authentication Service""",
    """({event_code}4768)""",
    """TargetUserName:(({user_upn}[^@,]+@[^,]+)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))),""",
    """TargetSid:({dest_user_sid}({user_sid}[^,]+)),""",
    """ServiceName:({service_name}[^,]+)""",
    """TicketOptions:({ticket_options}[^,]+),""",
    """TicketEncryptionType:({ticket_encryption_type}[^,]+),""",
    """Status:({failure_code}({result_code}[^,]+)),""",
    """IpAddress:(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,""",
    """({result}(Success|Failure) Audit)"""
  ]
  ParserVersion = "v1.0.0"


}
```