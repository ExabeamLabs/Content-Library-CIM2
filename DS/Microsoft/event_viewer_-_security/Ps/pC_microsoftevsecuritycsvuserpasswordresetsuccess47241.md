#### Parser Content
```Java
{
Name = microsoft-evsecurity-csv-user-password-reset-success-4724-1
   ParserVersion = v1.0.0
   Vendor = Microsoft
   Product = Event Viewer - Security
   TimeFormat = "MM/dd/yyyy hh:mm:ss a"
   Conditions = [ """アカウントのパスワードのリセットが試行されました。""" ]
   Fields = [
     """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({event_code}4724),""",
     """(?!\d+)({host}[\w\-.]+),([^,]*,)?アカウントのパスワードのリセットが試行されました。""",
     """ComputerName =({computer_name}[\w.\-]+)""",
     """EventCode=({event_code}\d+)""",
     """サブジェクト:.+?アカウント名:\s+({user}[\w\.\-]{1,40}\$?)\s+アカウント ドメイン:\s+({domain}.+?)\s+ログオン ID:""",
     """ログオン ID:\s+({login_id}[^\s]+)""",
     """ターゲット アカウント:.+?セキュリティ ID:\s+({user_sid}.+?)\s+アカウント名:\s+(?=\w)({dest_user}.+?)\s+アカウント ドメイン:\s+({dest_domain}.*?)\s*$"""
   ]
   DupFields = [ "computer_name->dest_host","computer_name->host" ]


}
```