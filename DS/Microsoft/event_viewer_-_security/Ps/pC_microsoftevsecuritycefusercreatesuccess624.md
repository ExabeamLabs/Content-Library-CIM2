#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-user-create-success-624"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|Microsoft|Microsoft Windows|"""
"""|Security:624|"""
]
Fields = [
"""({event_name}User Account Created)"""
"""({event_code}624)"""
"""\srt=({time}\d{13})"""
"""\ssntdom=({domain}[^\s]+)"""
"""\ssuser=({user}.+?)\s+\w+="""
"""\ssuid=\([^,]+,({login_id}[^\)]+)"""
"""\sdntdom=({account_domain}.+?)\s+\w+="""
"""\sduser=({account_name}.+?)\s+\w+="""
"""\sdvchost=({host}[^\s]+)"""
]
DupFields = [
"host->dest_host"
"account_name->dest_user"
]
ParserVersion = "v1.0.0"


}
```