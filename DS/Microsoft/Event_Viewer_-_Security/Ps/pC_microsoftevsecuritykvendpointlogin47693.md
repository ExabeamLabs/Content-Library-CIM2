#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-4769-3
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""LogType="WLS"""", """EventID="4769""""]
  Fields = [
    """Computer="+({host}[^"]+)"""",
    """"({time}\d\d\d\d\-\d{1,100}\-\d{1,100}T\d\d:\d\d:\d\d)""",
    """EventID="+({event_code}[^"]+)"""",
    """EventRecordID="+({event_id}[^"]+)"""",
    """TargetUserName ="+({user}[^@]+)@({web_domain}[^"]+)"""",
    """TargetLogonId="+({login_id}[^"]+)"""",
    """ServiceName ="+({dest_host}[^"]+\$)"""",
    """ServiceName ="+({service_name}[^"]+)"""",
    """IpAddress="+(::[\w]+:)?({src_ip}[a-fA-F:\d.]+)""",
    """Status="+({result_code}[^"]+)"""",
    """TicketEncryptionType="+({ticket_encryption_type}[^"]+)""""
    """TicketOptions="+({ticket_options}[^"]+)""""
  ]


}
```