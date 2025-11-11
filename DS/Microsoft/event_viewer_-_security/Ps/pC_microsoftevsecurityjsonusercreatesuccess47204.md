#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-user-create-success-4720-4
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy H:mm:ss a"
Conditions = [
  """"InstanceId":"4720""""
]
Fields = [
  """({event_name}A user account was created)"""
  """"MachineName":"({host}[\w\-.]+)"""
  """"TimeGenerated":"({time}[^"]*)"""
  """"InstanceId":"({event_code}[^"]+)"""
  """"4":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """"5":"({domain}[^"]+)"""
  """"6":"({login_id}[^"]+)"""
  """"2":"({account_id}[^"]+)"""
  """"0":"({dest_user}({account_name}[^"]+))"""
  """"1":"({dest_domain}({account_domain}[^"]+))"""
]
ParserVersion = "v1.0.0"


}
```