#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-remove-success-637"
Conditions = [
"""LogType="WLS""""
"""EventID="637""""
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