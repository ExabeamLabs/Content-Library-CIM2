#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-4776
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """4776""", """コンピューターがアカウントの資格情報の確認を試行しました。""" ]
  Fields = [
    """({time}\d\d\d\d\/\d\d\/\d\d[\s\t]+\d\d:\d\d:\d\d)\s+Microsoft-Windows-Security-Auditing""",
    """\s+ソース ワークステーション:\s+(\\+)?(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|(?:(?!NULL)({dest_host}[^\s]+)))\s+エラー コード:""",
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),4776,""",
    """ComputerName =({computer_name}[\w.\-]+)""",
    """ComputerName =({dest_host}[\w.\-]+)""",
    """\W4776\s+({host}[\w\-.]+)""",
    """(?!\d+)({host}[\w\-.]+),([^,]*,)?コンピューターがアカウントの資格情報の確認を試行しました。""",
    """({event_code}4776)""",
    """ログオン アカウント:\s+({user}[\w\.\-]{1,40}\$?)(?:@({domain}[^\s]+))?\s+ソース ワークステーション:""",
    """エラー コード:\s+({result_code}[\w\-]+)""" 
  ]
  DupFields = [ "computer_name->host" ]


}
```