#### Parser Content
```Java
{
Name = microsoft-evsecurity-csv-endpoint-login-success-4770
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """4770""", """Kerberos サービス チケットが更新されました。""", """アカウント名:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),4770,""",
    """ComputerName =({computer_name}[\w.\-]+)""",
    """(?!\d+)({host}[\w\-.]+),([^,]*,)?Kerberos サービス チケットが更新されました。""",
    """({event_code}4770)""",
    """アカウント名:\s+({user}[^@]+).+?\s+""",
    """アカウント ドメイン:\s+({domain}.+?)\s+サービス情報:""",
    """サービス名:\s+({service_name}.+?)\s+サービス ID:""",
    """サービス名:\s+({dest_host}.+?\$)\s+サービス ID:""",
    """チケット オプション:\s+({ticket_options}.+?)\s+チケット暗号化の種類:""",
    """チケット暗号化の種類:\s+({ticket_encryption_type}[^\s]+)""",
    """クライアント アドレス:\s+(::[\w]+:)?(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|::1)"""
    """クライアント アドレス:\s+(::[\w]+:)?({dest_ip}(?!::1)[a-fA-F:\d.]+)"""
  ]
  DupFields = [ "computer_name->host" ]


}
```