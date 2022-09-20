#### Parser Content
```Java
{
Name = questsoftware-caad-cef-group-member-remove-success-nestedmemberremove
     ParserVersion = "v1.0.0"
     Conditions = [
"""CEF:"""
"""Quest Software"""
"""|Change Auditor|"""
"""|Active Directory|"""
"""Nested member removed from group"""
     ]
     Fields = ${QuestParserTemplates.quest-change-auditor-events.Fields}[
       """msg=\s*[^\\]+[\\\/]*({account_id}[^(]+)[^=]+?was removed from group\s[^\\]+[\\\/]*({group_name}\S+)\s"""
     ]

quest-change-auditor-events = {
    Vendor = Quest Software
    Product = Quest Change Auditor for Active Directory
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Fields = [
"""start=({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)"""
"""dvchost=({host}[\w\-.]+)"""
"""domain=({domain}\S+)"""
"""categoryOutcome=({result}\S+)"""
"""src=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""userMail=({email_address}[^@=]+@[^\.]+[^\s]+)"""
"""suid=({user_sid}\S+)"""
"""suser=(({domain}[^\\]+)[\\\/]*)?({user}[^=]+?)\s\w+="""
"""event=({event_name}[^=]+?)\s\w+="""
"""msg=({additional_info}[^=]+?)\s*\w+="""
"""msg=Account unlocked for user\s*({user_ou}[^$]+?).\s*description="""

}
```