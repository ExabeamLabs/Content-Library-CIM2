#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-group-member-remove-success-4757"
Conditions = [
"""4757"""
"""<Data Name ='TargetSid'>"""
"""A member was removed from a security-enabled universal group"""
]
ParserVersion = "v1.0.0"

json-windows-events-1.Fields}[
    """({event_name}A user account was disabled)""",
    """"hostname"+:"+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({dest_host}[^"]+))""",
  
}
```