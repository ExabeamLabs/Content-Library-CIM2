#### Parser Content
```Java
{
Name = sangfor-ngaf-kv-alert-trigger-success-ips
  Vendor = Sangfor
  Product = Sangfor NGAF
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """type: IPS""", """<Identifier>ZC01_NTTDHK-FWL-002</Identifier>""" ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+[\+\-]\d+:\d+\s+({host}[\w\-.]+)""",
    """, policy name:\s*({policy_name}[^,]+)""",
    """, vulnerability ID:\s*({alert_id}[^,]+)""",
    """, vulnerability name:\s*({alert_name}[^,]+)""",
    """, Src IP:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """, Src port:\s*({src_port}\d+)""",
    """, dst IP:\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """, Dst port:\s*({dest_port}\d+)""",
    """, protocol:\s*({protocol}[^,]+)""",
    """, attack type:\s*({alert_type}[^,]+)""",
    """, threat level:\s*({alert_severity}[^,]+)""",
    """, action:\s*({action}[^,\s]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```