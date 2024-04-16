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
      """\srt=({time}\d{13})""",
      """({host}\S+)\s+CEF:\d+\|""",
      """\ssuser=({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s*(\w+=|$)""",
      """\sduser=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s*(\w+=|$)""",
      """\snitroSubject=({email_subject}[^\s].+?)\s*(\w+=|$)""",
      """\sact=({action}[^\s]+)\s*(\w+=|$)""",
      """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\sshost=(?:unknown|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}[\w\.\-]*|({src_host}[^\s]+))\s*(\w+=|$)""",
      """\scat=({alert_name}[^\s].+?)\s*(\w+=|$)"""
    ]
    DupFields = [ "alert_name->alert_type" ]
  

}
```