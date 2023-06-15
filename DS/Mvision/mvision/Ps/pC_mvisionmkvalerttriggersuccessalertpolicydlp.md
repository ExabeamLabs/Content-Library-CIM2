#### Parser Content
```Java
{
Name = mvision-m-kv-alert-trigger-success-alertpolicydlp
  Vendor = Mvision
  Product = Mvision
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
  ParserVersion = "v1.0.0"
  Conditions= [ """incidentGroup=Alert.Policy.Dlp""", """updatedOn="""" ]
  Fields = [
    """<\d+>\w+ \d\d \d\d:\d\d:\d\d ({host}[\w.\-]+)""",
    """\WupdatedOn="({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d+ \w+)""",
    """\WpolicyName ="({alert_name}[^"]+)""",
    """\WincidentId=({alert_id}\d+)""",
    """\WriskSeverity=({alert_severity}[^,]+)""",
    """\WactivityName =\[({alert_type}[^\[\]]+?)\]""",
    """\WsourceIps=(0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """\WactorId=({email_address}[^,]+)""",
    """\WFileSize=({bytes}\d+)""",
    """\WcontentItemId="({target}[^"]+)""",
    """\WcontentItemName ="({file_name}[^"]+)""",
    """\WinstanceName ="({src_host}[\w.-]+)"""",
    """\Wresponse=\[({action}[^\[\]]+?)\]""",
    """\W({additional_info}totalMatchCount=[^,]+)""",
  ]


}
```