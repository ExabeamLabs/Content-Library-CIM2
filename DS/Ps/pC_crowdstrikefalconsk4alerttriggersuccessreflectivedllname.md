#### Parser Content
```Java
{
Name = "crowdstrike-falcon-sk4-alert-trigger-success-reflectivedllname"
Conditions = [
""""event_simpleName":"ReflectiveDllLoaded""""
"""ReflectiveDllName"""
]
ParserVersion = "v1.0.0"

leef-crowdstrike-alert-t.Fields} [
    """CrowdStrike\|([^|]+\|){2}({alert_name}[^|]+)""",
    """\WdocAccessedFileName =({file_name}[^|"]+?(\.({file_ext}[^"\|.]+?))?)\s*(\||\w+=|$|"+\s*$)""",
    """\WdocAccessedFilePath=({file_dir}[^=]+?)\s*(\||\w+=|$|"+\s*$)""",
    """\Wdescription=({additional_info}[^=]+?)\s*(\||\w+=|$|"+\s*$)"""
  
}
```