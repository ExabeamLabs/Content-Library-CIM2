#### Parser Content
```Java
{
Name = "netskope-sc-json-file-auditlogevent"
Vendor = "Netskope"
Product = "Netskope Security Cloud"
TimeFormat = "epoch_sec"
Conditions = [
""""type": "admin_audit_logs""""
""""audit_log_event":"""
]
Fields = [
""""timestamp": ({time}\d{10})"""
""""audit_log_event": "({operation}[^"]+)""""
""""user": "(?![^\s]+@[^\s]+)({user}[^"\s]+)""""
""""user": "(?=[^\s]+@[^\s]+)({email_address}[^"\s@]+@({email_domain}[^"\s@]+))""""
]
DupFields = [
"operation->access"
]
ParserVersion = "v1.0.0"


}
```