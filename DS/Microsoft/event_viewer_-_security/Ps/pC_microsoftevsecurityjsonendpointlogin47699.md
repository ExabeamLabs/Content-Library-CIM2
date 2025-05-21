#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-4769-9
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """4769""", """Kerberos サービス チケットが要求されました。""" ]
  Fields = [ 
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),4769,""",
    """ComputerName =({computer_name}[\w.\-]+)""",
    """(?!\d+)({host}[\w\-.]+),([^,]*,)?Kerberos サービス チケットが要求されました。""",
    """({event_code}4769)""",
    """アカウント名:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[\w._\-]+)""",
    """サービス名:\s+({dest_host}\S+\$)\s+サービス ID:""",
    """サービス名:\s+({service_name}\S+)\s+サービス ID:""",
    """チケット オプション:\s+({ticket_options}\S+)\s+チケット暗号化の種類:""",
    """チケット暗号化の種類:\s+({ticket_encryption_type}\S+)\s+エラー コード:""",
    """クライアント アドレス:\s+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """エラー コード:\s+({result_code}[\w]+)""" 
  ]
  DupFields = [ "computer_name->host" ]


}
```