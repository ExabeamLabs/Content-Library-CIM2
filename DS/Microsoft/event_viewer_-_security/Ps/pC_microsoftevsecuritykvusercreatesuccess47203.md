#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-create-success-4720-3
   ParserVersion = v1.0.0
   Vendor = Microsoft
   Product = Event Viewer - Security
   TimeFormat = "MM/dd/yyyy hh:mm:ss a"
   Conditions = [  """ユーザー アカウントが作成されました。""" ]
   Fields = [
     """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({event_code}4720),""",
     """(?!\d+)({host}[\w\-.]+),([^,]*,)?ユーザー アカウントが作成されました。""",
     """ComputerName =({computer_name}[\w.\-]+)""",
     """EventCode=({event_code}\w+)""",
     """サブジェクト:.+?アカウント名:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+アカウント ドメイン:\s+({domain}[^\s]+).+?ログオ
ン ID:\s+({login_id}[^\s]+)""",
     """新しいアカウント:.+?セキュリティ ID:\s+({account_id}[^\s]+)\s+アカウント名:\s+({account_name}.+?)\s+アカウント ドメイン:\s+({account_domain}[^\s]+)"""
   ]
   DupFields = [ "computer_name->host" , "account_name->dest_user", "account_domain->dest_domain" ]


}
```