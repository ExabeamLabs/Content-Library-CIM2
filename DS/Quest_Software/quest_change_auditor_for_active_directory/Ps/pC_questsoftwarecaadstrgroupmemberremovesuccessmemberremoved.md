#### Parser Content
```Java
{
Name = questsoftware-caad-str-group-member-remove-success-memberremoved
     ParserVersion = "v1.0.0"
     Conditions = [ """ChangeAuditor""", """|Active Directory|""", """|Member removed from group|"""  ]
     DupFields = ${QuestParserTemplates.quest-auditor-events.DupFields}[ "object->group_name" ]

quest-auditor-events = {
    Vendor = Quest Software
    Product = Quest Change Auditor for Active Directory
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
    Fields = [
      """\|({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2}\.\d+)\|""",
      """\w{3}\s+\d{1,2}\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s""",
      """ChangeAuditor[^\|]+\|+(?:[^\|]+\|+){1}({object}[^\|]+)\|+(?:[^\|]+\|+){3}(({domain}[^\\\|]+?)\\+)?({user}[\w\.\-]{1,40}\$?)\|+({user_sid}[^\|]+?)\|+(({dest_domain}[^\\\|]+?)\\+)?({dest_user}\S+?)\|+({event_name}[^\|]+?)\|+({src_host}[^\|]+?)\|+({additional_info}[^\|]+)\|+(?:[^\|]+\|+){12}({app}[^\|]+)\|+({result}[^\|"]+?)(\\n)?(\||"|$| )"""
    ]
    DupFields = [ "event_name->operation" 
}
```