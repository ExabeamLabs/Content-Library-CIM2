#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-privilege-assign-success-4673-1"
Conditions = [ """"EventID":"4673"""", """A privileged service was called""" ]
ParserVersion = "v1.0.0"

json-windows-events-1.Fields}[
    """({event_name}A user account was disabled)""",
    """"hostname"+:"+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({dest_host}[^"]+))""",
  
}
```