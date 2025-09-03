#### Parser Content
```Java
{
Name = "crowdstrike-falcon-leef-alert-trigger-success-0"
Conditions = [
"""0|CrowdStrike|FalconHost|"""
"""cat=DetectionSummaryEvent"""
]
ParserVersion = "v1.0.0"

leef-crowdstrike-alert-t.Fields} [
    """CrowdStrike\|([^|]+\|){2}({alert_name}[^|]+)""",
    """\WdocAccessedFileName =({file_name}[^|"]+?(\.({file_ext}[^"\|.]+?))?)\s*(\||\w+=|$|"+\s*$)""",
    """\WdocAccessedFilePath=({file_dir}[^=]+?)\s*(\||\w+=|$|"+\s*$)""",
    """\Wdescription=({additional_info}[^=]+?)\s*(\||\w+=|$|"+\s*$)"""
  
}
```