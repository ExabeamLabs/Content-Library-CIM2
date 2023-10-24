#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-app-login-success-smartdashboard
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "ddMMMyyyy HH:mm:ss"
  Conditions = [ """|product=SmartDashboard|""", """|Subject=Administrator Login|""" ]
  Fields = [
    """\|Administrator=({user}[\w\.\-]{1,40}\$?)\|""",
    """\|time=({time}\d+\w+\d\d\d\d \d+:\d+:\d+)""",
    """\|client_ip=(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w.\-]+))\|""",
    """\|Machine=({host}[^\|]+)\|"""
    """\|Additional Info=({additional_info}[^\|]+)\|""",
    """\|product=({app}SmartDashboard)"""
  ]
  ParserVersion = v1.0.0


}
```