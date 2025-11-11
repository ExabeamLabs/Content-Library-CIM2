#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-4769-3
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = ["""LogType="WLS"""", """EventID="4769""""]
  Fields = [
    """({time}\w+ \d+ \d+:\d+:\d+( \d\d\d\d)?)"""
    """Computer="+({host}[^"]+)"""",
    """"({time}\d\d\d\d\-\d{1,100}\-\d{1,100}T\d\d:\d\d:\d\d)""",
    """EventID="+({event_code}[^"]+)"""",
    """EventRecordID="+({event_id}[^"]+)"""",
    """TargetUserName ="+({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({dest_domain}({domain}[^"]+))"""",
    """TargetLogonId="+({dest_login_id}({login_id}[^"]+))"""",
    """ServiceName ="+({dest_host}[\w\-.]+\$)"""",
    """ServiceName ="+({service_name}[^"]+)"""",
    """IpAddress="+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Status="+({result_code}[^"]+)"""",
    """TicketEncryptionType="+({ticket_encryption_type}[^"]+)""""
    """TicketOptions="+({ticket_options}[^"]+)""""
  ]


}
```