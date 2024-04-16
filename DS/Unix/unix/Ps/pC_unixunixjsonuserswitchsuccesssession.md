#### Parser Content
```Java
{
Name = "unix-unix-json-user-switch-success-session"
Product = "Unix"
ExtractionType = json
Conditions = [
""""ident":"sudo"""
"""pam_unix(sudo:session): session"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```