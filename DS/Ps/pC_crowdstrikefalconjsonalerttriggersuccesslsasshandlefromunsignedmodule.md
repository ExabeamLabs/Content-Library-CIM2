#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-alert-trigger-success-lsasshandlefromunsignedmodule"
Conditions = [
""""event_simpleName\":\"LsassHandleFromUnsignedModule\"""", """\"aip\"""", """\"aid\""""
]
ExtractionType = json
ParserVersion = "v1.0.0"

leef-crowdstrike-alert-t.Fields} [
    """CrowdStrike\|([^|]+\|){2}({alert_name}[^|]+)""",
    """\WdocAccessedFileName =({file_name}[^|"]+?(\.({file_ext}[^"\|.]+?))?)\s*(\||\w+=|$|"+\s*$)""",
    """\WdocAccessedFilePath=({file_dir}[^=]+?)\s*(\||\w+=|$|"+\s*$)""",
    """\Wdescription=({additional_info}[^=]+?)\s*(\||\w+=|$|"+\s*$)"""
  
}
```