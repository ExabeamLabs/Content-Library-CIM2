#### Parser Content
```Java
{
Name = symantec-endpointprotection-cef-alert-trigger-success-symantec
    Vendor = Symantec
    Product = Symantec Endpoint Protection
    TimeFormat = "epoch"
    Conditions = [ """CEF""", """|Symantec|Symantec Endpoint Protection|""" ]
    Fields = [
      """"collector_name":"({host}[^"]+)"""",
      """\Wrt=({time}\d{13})""",
      """"feature_name":"({alert_name}[^"]+)"""",
      """"severity_id":({alert_severity}\d+)""",
      """\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\Wdvchost=({host}.+?)(\s+\w+=|\s*$)""",
      """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\Wshost=({src_host}.+?)(\s+\w+=|\s*$)""",
      """"user_name":"({user}[^"]+)"""",
      """"type":"({alert_type}[^"]+)"""",
      """"device_domain":"({domain}[^"]+)"""",
      """"src_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"src_port":"({src_port}\d+)""",
      """"dst_port":"({dest_port}\d+)""",
      """"src_name":"({src_host}[^"]+)"""",
      """"dst_ip":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """"device_os_name":"({os}[^"]+)"""",
      """"product_name":"({product_name}[^"]+)"""",
    ]
	ParserVersion = "v1.0.0"
  

}
```