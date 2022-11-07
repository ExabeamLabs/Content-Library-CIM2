#### Parser Content
```Java
{
Name = barracuda-esg-cef-app-activity-success-scan
    ParserVersion = v1.0.0
    Vendor = Barracuda
    Product = Barracuda Email Security Gateway
    TimeFormat = "epoch"
    Conditions = [ """|McAfee|ESM|""", """nitroSubject=""", """Barracuda""" ]
    Fields = [
      """\srt=({time}\d+)""",
      """({host}\S+)\s+CEF:\d+\|""",
      """\ssuser=({email_address}[^\s]+)\s*(\w+=|$)""",
      """\sduser=({dest_email_address}[^\s]+)\s*(\w+=|$)""",
      """\snitroSubject=({email_subject}[^\s].+?)\s*(\w+=|$)""",
      """\sact=({action}[^\s]+)\s*(\w+=|$)""",
      """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\sshost=(?:unknown|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}[\w\.\-]*|({src_host}[^\s]+))\s*(\w+=|$)""",
      """\scat=({alert_name}[^\s].+?)\s*(\w+=|$)"""
    ]
    DupFields = [ "alert_name->alert_type" ]
  

}
```