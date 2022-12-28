#### Parser Content
```Java
{
Name = mcafee-idps-str-alert-trigger-success-ivrelevance
  Vendor = McAfee
  Product = McAfee IDPS
  TimeFormat = "yyyy-MM-dd HH:mm:ss z"
  Conditions = [ """ AlertLog: |""", """|$IV_RELEVANCE$|""" ]
  Fields = [
    """\|({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d \w+)\|"({alert_name}[^"]+)"\|[^\|]*\|(N/A|({alert_severity}[^\|]+))(\|[^\|]*){3}\|({host}[^\|]+)\|[^\|]*\|(N/A|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\|(N/A|({=src_port}\d+))\|(N/A|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\|(N/A|({=dest_port}\d+))\|({alert_type}[^\|]+\|[^\|]+)\|({direction}[^\|]+)\|(n/a|({action}[^\|]+))(\|[^\|]*){2}\|(N/A|({protocol}[^\|]+))""",
  ]
  ParserVersion = "v1.0.0"


}
```