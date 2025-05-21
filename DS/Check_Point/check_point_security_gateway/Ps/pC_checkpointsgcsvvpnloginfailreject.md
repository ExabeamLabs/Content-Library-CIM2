#### Parser Content
```Java
{
Name = "checkpoint-sg-csv-vpn-login-fail-reject"
Vendor = "Check Point"
Product = "Check Point Security Gateway"
TimeFormat = "ddMMMyyyy,HH:mm:ss"
Conditions = [
  """,alert,reject,"""
]
Fields = [
  """({time}\d+\w+\d\d\d\d,\d+:\d+:\d+)(\s+(\+|\-)\d+)?,(|({host}[^,]+)),alert,reject,([^,]*,){8}(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),(|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),([^,]*,){14}\s*(|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),(|({failure_reason}[^,]+?))\s*,"""
]
ParserVersion = "v1.0.0"


}
```