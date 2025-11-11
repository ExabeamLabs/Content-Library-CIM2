#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-delete-fail-locked"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""__li_source_path="""
"""A user account was locked out"""
"""eventid="4740""""
]
Fields = [
"""({event_name}A user account was locked out)"""
"""\W__li_source_path=\"({host}[\w\.-]+)\""""
"""({event_code}4740)"""
"""\Weventrecordid=\"({event_id}\d+)\""""
"""Subject:.+?Account Name:\s+({src_user}.+?)\s+Account Domain:\s+(?=\w)({domain}({src_domain}.+?))\s+Logon ID:\s+({login_id}[^\s]+)"""
"""Locked Out:\s+Security ID:\s+(%\{)?({user_sid}([\w\d\-]+?)|([^\s]+))\}?\s+Account Name:\s+(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Additional"""
"""Caller Computer Name:\s+(\\+)?({src_host}[^\#\s\",]+)"""
]
ParserVersion = "v1.0.0"


}
```