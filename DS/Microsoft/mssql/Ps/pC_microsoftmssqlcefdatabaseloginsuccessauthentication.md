#### Parser Content
```Java
{
Name = microsoft-mssql-cef-database-login-success-authentication
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = MSSQL
  TimeFormat = "epoch"
  Conditions = [
"""CEF:""",
"""|Microsoft|SQL Server|""",
"""categoryBehavior=/Authentication/Verify"""
  ]
  Fields = [
    """\sduser=(({domain}[^=\\\/]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*$)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """cs3=({service_name}[^\s]+)"""
    """\sdestinationServiceName =(|({service_name}.+?))(\s+\w+=|\s*$)""",
    """\sshost=(|({host}.+?))(\s+\w+=|\s*$)""",
    """\srt=({time}\d{13})""",
    """\scategoryOutcome=/({result}.+?)(\s+\w+=|\s*$)""",
  ]


}
```