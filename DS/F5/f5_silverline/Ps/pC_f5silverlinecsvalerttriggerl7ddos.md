#### Parser Content
```Java
{
Name = f5-silverline-csv-alert-trigger-l7ddos
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 Silverline
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """type = l7ddos,""", """, action=""", """, reason=""", """, request_status=""" ]
  Fields = [
    """type\s*=\s*({alert_type}l7ddos)""",
    """action=({action}[^,]+)""",
    """client_ip=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """reason=({alert_name}[^,]+?)\s*$""",
    ]


}
```