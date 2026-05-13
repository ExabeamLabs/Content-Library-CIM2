#### Parser Content
```Java
{
Name = trendmicro-ds-leef-alert-trigger-winevtloginspection
  Vendor = Trend Micro
  Product = Deep Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """LEEF:""", """|Trend""", """|Deep Security Agent|""", """cat=Log Inspection""", """WinEvtLog""", """desc="""  ]
  Fields = [
    """\d\d:\d\d:\d\d\S*\s({host}[\w\-.]+) LEEF:""",
    """dvc=({host}[A-Fa-f:\d.]+)""",
    """shost=({src_host}[\w\-.]+)""",
    """AUDIT_\w+\(({event_code}\d+)\)""",
    """desc=({event_name}.+?)\s*\w+=""",
    """sev=({alert_severity}\d+)""",
    """cn1=({asset_id}\d+)""",
    """cat=({alert_type}[^#]+)"""
  ]
ParserVersion = "v1.0.0"  


}
```