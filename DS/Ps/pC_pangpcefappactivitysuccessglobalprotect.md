#### Parser Content
```Java
{
Name = pan-gp-cef-app-activity-success-globalprotect
  ParserVersion = "v1.0.0"
  Conditions = [ """,GLOBALPROTECT,"""]
  Fields = ${PaloAltoParsersTemplates.raw-pan-vpn-event.Fields}[
    """,({app}GLOBALPROTECT),""",
    """GLOBALPROTECT,([^,]*,){10}({src_host}[\w\-.]+),"""
    """GLOBALPROTECT,([^,]*,){18}(|(?i)any|0|({os}[^,]*)),"""
    """Private IP:\s?({src_translated_ip}[^,\s]+)""",
    """User\s*name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\.?(\s|,|"|$)""",
    """SYSTEM,([^,]*,){9}({severity}[^,]+),""",
    """({event_category}SYSTEM)""",
    """SYSTEM,({event_subtype}[^,]+),""",
    """,({asset_id}\d+),SYSTEM,""",
    """SYSTEM,(?:[^,]*,){10}"*({additional_info}[^",]+?)(?:\.*"|\.\s|\.*,|\s(\d{1,3}\.){3}\d{1,3}:\d+)""",
    """,GLOBALPROTECT,([^,]*,){48}({device_name}[^,]+)"""
  ]


}
```