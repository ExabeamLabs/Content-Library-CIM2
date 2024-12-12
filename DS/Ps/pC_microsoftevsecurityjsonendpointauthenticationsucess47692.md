#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-authentication-sucess-4769-2"
Conditions = [
""""event-id":4769"""
""""message":"A Kerberos service ticket was requested"""
]
ParserVersion = "v1.0.0"

s-xml-windows-member.Fields}[
    """({event_name}A member was added to a security-enabled global group)"""
    """<Message>({event_name}[^:=<.]+)\."""
    """A member was added to a security-enabled ({group_type}[^\s]+) group""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Computer>({host}[\w\-.]+)<\/Computer>"""
    
}
```