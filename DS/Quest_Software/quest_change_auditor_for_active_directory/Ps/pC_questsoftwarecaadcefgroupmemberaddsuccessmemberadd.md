#### Parser Content
```Java
{
Name = questsoftware-caad-cef-group-member-add-success-memberadd
     ParserVersion = "v1.0.0"
     Conditions = [
"""CEF:"""
"""Quest Software"""
"""|Change Auditor|"""
"""|Active Directory|"""
"""Member added to group"""
      ]
     Fields = ${QuestParserTemplates.quest-change-auditor-events.Fields}[
       """msg=[^\\]+[\\\/]*({account_id}[^(]+)[^=]+?was added to group\s[^\\]+[\\\/]*({group_name}\S+)\s"""
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
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""userMail=({email_address}[^@=]+@[^\.\s]+\.[^\]\s"\\,\|]+)"""
"""suid=({user_sid}\S+)"""
"""suser=(({domain}[^\\]+)[\\\/]*)?({user}[^=]+?)\s\w+="""
"""event=({event_name}[^=]+?)\s\w+="""
"""msg=({additional_info}[^=]+?)\s*\w+="""
"""msg=Account unlocked for user\s*({user_ou}[^$]+?).\s*description="""

}
```