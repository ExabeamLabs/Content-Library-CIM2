#### Parser Content
```Java
{
Name = microsoft-evsecurity-csv-endpoint-login-4768
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """4768""", """Kerberos 認証チケット (TGT) が要求されました。""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),4768,""",
    """ComputerName =({computer_name}[\w.\-]+)""",
    """({host}(?!\d+)[\w\-.]+),([^,]*,)?Kerberos 認証チケット \(TGT\) が要求されました。""",
    """({event_code}4768)""",
    """アカウント名:\s+({user}[^@]+?)(?:@([^\s]+))?\s+提供された領域名:""",
    """クライアント アドレス:\s+(::[\w]+:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """結果コード:\s+({result_code}[\w]+)""",
    """提供された領域名:\s+({domain}[^\s]+)""",
    """ユーザー ID:\s+(?:NULL SID|({user_sid}.+?))\s+サービス情報:"""
  ]
  DupFields = [ "computer_name->host" ]


}
```