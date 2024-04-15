#### Parser Content
```Java
{
Name = "hp-arubawc-cef-endpoint-login-success-radiusaccounting"
Product = "Aruba Wireless controller"
Conditions = [
"""|Aruba Networks|ClearPass|"""
"""|RADIUS Accounting|"""
]
ParserVersion = "v1.0.0"

sap-login-activity = {
  Vendor = SAP
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """dvchost=({host}[^\s]+)""",
    """dvc=({host_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """end=({time}\w+\s\d+\s\d+\s\d\d:\d\d:\d\d)""",
    """SECUDE\|C-Bus\|[^\|]+\|(|({activity_id}[^\|]+))\|(|({event_name}[^\|]+))\|""",
    """suser=({user}[^\s]+)\s\w+=""",
    """shost=(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+))|({src_host}[^\s]+))""",
    """cat=({category}[^=]+?)(\s\w+=|\s*$)""",
    """requestClientApplication=({app}[^"]+?)\s\w+=""",
    """msg=({additional_info}[^"]+?)\s+\w+="""
  ]
  DupFields = [ "activity_id->event_code" 
}
```