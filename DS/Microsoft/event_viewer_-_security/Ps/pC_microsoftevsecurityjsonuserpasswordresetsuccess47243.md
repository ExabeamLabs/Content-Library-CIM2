#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-password-reset-success-4724-3"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy H:mm:ss a"
Conditions = [
""""InstanceId":"4724""""
]
Fields = [
"""({event_name}An attempt was made to reset an account's password)"""
""""MachineName":"({host}[\w\-.]+)"""
""""TimeGenerated":"({time}[^"]*)"""
""""InstanceId":"({event_code}[^"]+)"""
""""4":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
""""5":"({domain}[^"]+)"""
""""6":"({login_id}[^"]+)"""
""""3":"({user_sid}[^"]+)"""
""""2":"({dest_user_sid}[^"]+)"""
""""0":"({dest_user}[^"]+)"""
""""1":"({dest_domain}[^"]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```