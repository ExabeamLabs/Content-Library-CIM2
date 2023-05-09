#### Parser Content
```Java
{
Name = symantec-endpointprotection-cef-endpoint-notification-success-infosubmitted
    Vendor = Symantec
    Product = Symantec Endpoint Protection
    ParserVersion = v1.0.0
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """|Symantec|""", """Information submitted to Symantec""", """"collector_name"""" ]
    Fields = [
      """\d\d:\d\d:\d\d\s({host}[^\s]+) CEF:""",
      """"arr_time":"({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.\d{3}Z)"""",
      """({event_name}Information submitted to Symantec)""",
      """suser=({user}[^=]+?)\s*\w+=""",
      """\sdvchost=({host}[\w\-.]+)""",
	  """agt=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))\s"""
      """\|Symantec\|([^\|]*\|){3}({additional_info}[^\|]+)\|"""   
    ]


}
```