#### Parser Content
```Java
{
Name = "cyberark-pam-kv-alert-trigger-success-keystrokelogging"
Conditions = [
"""%CYBERARK:"""
"""Message="Keystroke logging""""
""";Safe="""
]
DupFields = [
"operation->alert_name"
"operation->alert_type"
]
ParserVersion = "v1.0.0"


}
```