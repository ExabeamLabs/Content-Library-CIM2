#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-add-success-4756-1"
Conditions = [
"""4756"""
"""<Data Name"""
"""'TargetSid'>"""
"""A member was added to a security-enabled universal group"""
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