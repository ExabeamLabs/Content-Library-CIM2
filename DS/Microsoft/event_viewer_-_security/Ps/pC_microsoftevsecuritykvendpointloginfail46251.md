#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-fail-4625-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""__li_source_path="""
"""An account failed to log on"""
"""eventid="4625""""
]
Fields = [
"""({event_name}An account failed to log on)"""
"""__li_source_path="({host}[^"]+)""""
"""__li_source_path="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
"""({event_code}4625)"""
"""An account failed to log on.+?Account Name:\s+(?=\w)({src_user}.+?)\s+Account Domain:"""
"""An account failed to log on.+?Account Domain:\s+(?=\w)({src_domain}.+?)\s+Logon ID:"""
"""Logon Type:\s+({login_type}\d+)"""
"""Account For Which Logon Failed:\s+Security ID:\s+({user_sid}[^\s]+)\s+Account"""
"""Logon Failed:.+?Account Name:\s+(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:"""
"""Logon Failed:.+?Account Domain:\s+(?=\w)({domain}.+?)\s+Failure Information"""
"""Sub Status:\s+({result_code}[^\s]+) """
"""Source Network Address:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""Logon Process:\s+({auth_process}[^\s]+)\s+Authentication Package:\s+({auth_package}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```