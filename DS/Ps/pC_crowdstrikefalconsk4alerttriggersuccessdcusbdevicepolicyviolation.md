#### Parser Content
```Java
{
Name = "crowdstrike-falcon-sk4-alert-trigger-success-dcusbdevicepolicyviolation"
Conditions = [
""""event_simpleName":"DcUsbDevicePolicyViolation""""
]
ParserVersion = "v1.0.0"

leef-crowdstrike-alert-t.Fields} [
    """CrowdStrike\|([^|]+\|){2}({alert_name}[^|]+)""",
    """\WdocAccessedFileName =({file_name}[^|"]+?)\s*(\||\w+=|$|"+\s*$)""",
    """\WdocAccessedFilePath=({file_dir}[^=]+?)\s*(\||\w+=|$|"+\s*$)""",
    """\Wdescription=({additional_info}[^=]+?)\s*(\||\w+=|$|"+\s*$)"""
  
}
```