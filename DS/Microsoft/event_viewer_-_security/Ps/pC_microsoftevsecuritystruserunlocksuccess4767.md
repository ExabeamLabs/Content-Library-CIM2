#### Parser Content
```Java
{
Name = "microsoft-evsecurity-str-user-unlock-success-4767"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["MMM dd HH:mm:ss yyyy", "MM/dd/yyyy hh:mm:ss a"]
Conditions = [
"""A user account was unlocked"""
"""Account Name:"""
]
Fields = [
"""({event_name}A user account was unlocked)"""
"""({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+"""
"""({event_code}4767)"""
"""(?i)(success|failure|audit)\s+\w+\s+(::ffff:)?({host}[\w\-.]+)"""
"""Computer(Name)?\s*\\*\"?(=|:|>)\s*\"{0,20}(::ffff:)?({host}[\w\.-]+)(\s|,|\"|</Computer>|$)"""
"""(?i)\w+\s*\d+\s\d+:\d+:\d+\s+(::ffff:)?(am|pm|({host}[\w\-.]+))\s\w"""
"""Subject:.+?Account Name:\s*({user}[\w\.\-]{1,40}\$?)\s*Account Domain:\s*({domain}.+?)\s*Logon ID:\s*({login_id}.+?)\s*Target Account:"""
"""Target Account:(\\t|\\r|\\n|\s)*Security ID:(\\t|\\r|\\n|\s)*({user_sid}.+?)(\\t|\\r|\\n|\s)*Account Name:(\\t|\\r|\\n|\s)*({dest_user}[\w\.\-]{1,40}\$?)(\\t|\\r|\\n|\s)*Account Domain:(\\t|\\r|\\n|\s)*({dest_domain}.+?)(\w+=|$|"|\s)"""
"""({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
]
ParserVersion = "v1.0.0"


}
```