#### Parser Content
```Java
{
Name = microsoft-mssql-cef-database-login-success-authentication
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = SQL Server
  TimeFormat = "epoch"
  Conditions = [
"""CEF:""",
"""|Microsoft|SQL Server|""",
"""categoryBehavior=/Authentication/Verify"""
  ]
  Fields = [
    """\sduser=(({domain}[^=\\\/]+)[\\\/]+)?({user}[^\\\/=]+?)(\s+\w+=|\s*$)""",
    """\ssrc=({src_ip}[a-fA-F\d.:]+)""",
    """cs3=({service_name}[^\s]+)"""
    """\sdestinationServiceName =(|({service_name}.+?))(\s+\w+=|\s*$)""",
    """\sshost=(|({host}.+?))(\s+\w+=|\s*$)""",
    """\srt=({time}\d+)""",
    """\scategoryOutcome=/({result}.+?)(\s+\w+=|\s*$)""",
  ]


}
```