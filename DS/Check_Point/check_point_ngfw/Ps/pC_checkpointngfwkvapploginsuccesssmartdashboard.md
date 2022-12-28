#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-app-login-success-smartdashboard
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "ddMMMyyyy HH:mm:ss"
  Conditions = [ """|product=SmartDashboard|""", """|Subject=Administrator Login|""" ]
  Fields = [
    """\|Administrator=({user}[^\|]+)\|""",
    """\|time=({time}\d+\w+\d\d\d\d \d+:\d+:\d+)""",
    """\|client_ip=(?:({src_ip}[a-fA-F\d.:]+)|({src_host}[\w.\-]+))\|""",
    """\|Machine=({host}[^\|]+)\|"""
    """\|Additional Info=({additional_info}[^\|]+)\|""",
    """\|product=({app}SmartDashboard)"""
  ]
  ParserVersion = v1.0.0


}
```