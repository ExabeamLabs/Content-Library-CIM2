#### Parser Content
```Java
{
Name = epic-siem-leef-app-activity-securitysiem
  Vendor = Epic
  Product = Epic SIEM
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """LEEF:""", """|Epic|Security-SIEM|""" ]
  Fields = [
    """({host}[\w.\-]+) LEEF:([^\|]*\|)({app}[^\|]+)\|([^\|]*\|){2}({operation}[^\|]+)""",
    """({host}[\w.\-]+),"+LEEF:[^\|]+\|({app}[^\|]+)\|([^\|]+\|){2}({operation}[^\|]+)""",
    """shost=({src_host}[^=]+?)(\s+\w+=|\s*$)""",
    """usrName =({user_id}[^=]+?)(\s+\w+=|\s*$)""",
    """usrName =\w+-({full_name}[^=]+?)\s*-"""
    """resource=\s*({resource}[^=]+?)(\s+\w+=|\s*$)""",
    """devTime=({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)""",
    """E3MID=({event_id}[^=]+?)(\s+\w+=|\s*$)""",
    """LOGIN_LDAP_ID=({user}[^=]+?)(\s+\w+=|\s*$)""",
    """IP=(?:({dest_ip}[a-fA-F\d.:]+)\/)?({src_ip}[a-fA-F\d.:]+)""",
    """LOGINERROR=({failure_reason}[^\s]*?)(\s+\w+=|\s*$)""",
    """ERRMSG=({failure_reason}[^\s]*?)(\s+\w+=|\s*$)""",
    """UID=({user_id}[^=]+?)(\s+\w+=|\s*$)""",
    """NEWDEPARTMENT=({object}[^=]+?)(\s+\w+=|\s*$)""",
    """BTGNOACCESSREAS=({additional_info}[^=]+?)(\s+\w+=|\s*$)""",
    """LEEF:[^\|]+\|({app}[^\|]+)\|([^\|]+\|){2}({operation}[^\|]+)"""
  ]
  ParserVersion = v1.0.0


}
```