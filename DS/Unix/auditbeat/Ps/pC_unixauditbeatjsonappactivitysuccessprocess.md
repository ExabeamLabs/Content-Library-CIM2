#### Parser Content
```Java
{
Name = "unix-auditbeat-json-app-activity-success-process"
Vendor = "Unix"
Product = "Auditbeat"
TimeFormat = "epoch"
Conditions = [
"""changed-identity-of"""
"""process"""
"""audit_id"""
]
Fields = [
"""time"+:"+({time}\d{13})"""
"""hostname"+:"+({host}[^"]+)"""
"""actor_secondary"+:"+({account}[^"]+)"""
"""actor_primary"+:"+({user}[\w\.\-]{1,40}\$?)"""
"""audit_name"+:"+({user}[\w\.\-]{1,40}\$?)"""
"""audit_id"+:"+({audit_id}[\d]+)"""
""""pid"+:"+({process_id}[^"]+)"""
""""ppid"+:"+({parent_process_id}[^"]+)"""
"""title"+:"+({process_command_line}[^"]+)"""
"""result"+:"+({result}[^"]+)"""
"""event_type"+:"+({operation_type}[^"]+)"""
"""application"+:"+({app}[^"]+)"""
"""category"+:"+({category}[^"]+)"""
"""syscall"+:"+({syscall}[^"]+)"""
"""effective_group_id"+:"+({group_id}[^"]+)"""
"""tags"+:"+\[({tags}[^"]+)\]"""
"""os"+:"+({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin|Ubuntu)"""
]
ParserVersion = "v1.0.0"


}
```