#### Parser Content
```Java
{
Name = microsoft-evsecurity-csv-endpoint-login-fail-4625
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","MM/dd/yyyy hh:mm:ss a"]
  Conditions = [ """アカウントがログオンに失敗しました。""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({event_code}4625),""",
    """(?!\d+)({host}[\w\-.]+),([^,]*,)?アカウントがログオンに失敗しました。""",
    """ComputerName =({computer_name}[\w.\-]+)""",
    """EventCode=({event_code}\d+)""",
    """アカウントがログオンに失敗しました。.+?アカウント名:\s+(?=\w)({src_user}.+?)\s+アカウント ドメイン:""",
    """アカウントがログオンに失敗しました。.+?アカウント ドメイン:\s+(?=\w)({src_domain}.+?)\s+ログオン ID:""",
    """ログオン タイプ:\s+({login_type}\d+)""",
    """ログオンを失敗したアカウント:\s+セキュリティ ID:\s+({user_sid}[^\s]+)\s+アカウント名:""",
    """ログオンを失敗したアカウント:.+?アカウント名:\s+(?=\w)(({user_upn}[^@"]+@({domain}[^\."]+\.[^"]+))(?<!local)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({=domain}[^"]+)?)))\s+アカウント ドメイン:""",
    """ログオンを失敗したアカウント:.+?アカウント ドメイン:\s+(?=\w)({domain}.+?)\s+エラー情報:""",
    """サブ ステータス:\s+({result_code}[^\s]+) """,
    """ソース ネットワーク アドレス:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """ログオン プロセス:\s+({auth_process}[^\s]+)\s+認証パッケージ:\s+({auth_package}[^\s]+)"""
  ]
  DupFields = [ "host->dest_host","computer_name->host" ]


}
```