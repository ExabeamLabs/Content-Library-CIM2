#### Parser Content
```Java
{
Name = tyco-ccure-cef-app-login-success-operatorlogin
  ParserVersion = v1.0.0
  Vendor = Tyco
  Product = CCURE Building Management System
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|C-CURE|""", """|Operator Login"""]
  Fields = [
     """src=({host}[^\s]+)""",
     """\|start=({time}\d{13})""",
     """({app}C-CURE)""",
     """\ssuid=(?:Unknown|(({domain}[^\\]+)\\?)?({user}.+?))\s(\w+=|$)""",
     """\ssuser=(?:|({full_name}.+?))\s(\w+=|$)"""
    ]


}
```