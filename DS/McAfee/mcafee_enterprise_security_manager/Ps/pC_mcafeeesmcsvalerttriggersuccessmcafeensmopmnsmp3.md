#### Parser Content
```Java
{
Name = mcafee-esm-csv-alert-trigger-success-mcafeensmopmnsmp3
  Vendor = McAfee
  Product = McAfee Enterprise Security Manager
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """|McAfee|ESM|""", """deviceExternalId=McAfee_NSM_OPMNSMP3""" ]
  Fields = [
    """\|McAfee\|ESM\|([^|]+?\|){2}({alert_name}[^|]+)\|""",
    """\Wrt=({time}\d{13})""",
    """\Wproto=({protocol}.*?)\s+(\w+=|$)""",
    """\Wcat=({alert_type}.*?)\s+(\w+=|$)""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wspt=({src_port}\d+)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wshost=({src_host}.*?)\s+(\w+=|$)""",
    """\WnitroCategory=({threat_category}.*?)\s+(\w+=|$)""",
    """\Wsntdom=({domain}.*?)\s+(\w+=|$)"""
  ]
  ParserVersion = "v1.0.0"


}
```