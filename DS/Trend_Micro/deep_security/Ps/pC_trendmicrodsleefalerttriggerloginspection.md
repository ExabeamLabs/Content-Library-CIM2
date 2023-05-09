#### Parser Content
```Java
{
Name = trendmicro-ds-leef-alert-trigger-loginspection
    Vendor = Trend Micro
    Product = Deep Security
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """LEEF:""", """|Trend Micro|Deep Security Agent|""", """cat=Log Inspection""", """Windows System ArgumentsOutOfRange Error found""", """(1001)""" ]
    Fields = [
      """\d\d:\d\d:\d\d ({host}[\w\-.]+) LEEF:""",
      """dvc=({host}[A-Fa-f:\d.]+)""",
      """shost=({src_host}[\w\-.]+)""",
      """({event_code}1001)""",
      """({event_name}Windows System ArgumentsOutOfRange Error found)""",
      """sev=({alert_severity}\d+)""",
      """cn1=({asset_id}\d+)""",
      """cat=({alert_type}[^#]+)"""
# appcrash_response is removed
# problem_signature is removed
# report_id is removed
# report_status is removed
    ]
  ParserVersion = "v1.0.0"
      DupFields = [ "event_name->alert_name"]
  

}
```