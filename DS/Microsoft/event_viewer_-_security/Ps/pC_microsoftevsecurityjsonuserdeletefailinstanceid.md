#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-delete-fail-instanceid"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy H:mm:ss a"
Conditions = [
""""InstanceId":"4740""""
]
Fields = [
""""TimeGenerated":"({time}[^\"]*)"""
"""({event_name}A user account was locked out)"""
""""MachineName":"({host}[\w\-.]+)"""
""""InstanceId":"({event_code}[^\"]*)"""
""""4":"({src_user}[^\"]*)"""
""""5":"({domain}({src_domain}[^\"]*))"""
""""6":"({login_id}[^\"]*)"""
""""2":"({user_sid}[^\"]*)"""
""""0":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
""""1":"({src_host}[^\"]*)"""
]
ParserVersion = "v1.0.0"


}
```