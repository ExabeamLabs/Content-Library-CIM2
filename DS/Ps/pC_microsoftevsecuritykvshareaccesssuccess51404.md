#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-share-access-success-5140-4"
Conditions = [
"""LogType="WLS""""
"""EventID="5140""""
]
ParserVersion = "v1.0.0"

s-xml-windows-member.Fields}[
    """<Data Name(\\)?=('|")SubjectUserName('|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>""",
    """<Data Name(\\)?=('|")SubjectDomainName('|")>({src_domain}({domain}[^<]+))</Data>""",
    """<Data Name(\\)?=('|")RemoteIPAddress('|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """<Data Name(\\)?=('|")LocalIPAddress('|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<""",
    """<Data Name(\\)?=('|")RemotePort('|")>({dest_port}\d+)""",
    """<Data Name(\\)?=('|")LocalPort('|")>({src_port}\d+)""",
    """({event_name}A member was added to a security-enabled global group)"""
    """<Message>({event_name}[^:=<.]+)\."""
    """A member was added to a security-enabled ({group_type}[^\s]+) group""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Computer>({host}[\w\-.]+)<\/Computer>"""
    """<Data Name(\\)?=('|")TargetUserName('|")>({group_name}[^<]+)</Data>""",
    
}
```