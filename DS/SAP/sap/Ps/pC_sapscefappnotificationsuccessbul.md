#### Parser Content
```Java
{
Name = sap-s-cef-app-notification-success-bul
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|SECUDE|C-Bus|""", """|BUL|""" ]

sap-activity = {
  Vendor = SAP
  Product = SAP
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """end=({time}\w{3,4} \d{1,2} \d{4} \d{1,2}:\d{1,2}:\d{1,2})""",
    """dvchost=({host}[^\s]+)""",
    """suser=({user}[\w\.\-]{1,40}\$?)""",
    """shost=(({src_ip}((([0-9a-fA-F.:]{1,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w.-]+))\s""",
    """msg=({additional_info}[^=]+?)\s*\w+=""",
    """dvc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """duser=({account_name}[^\s]+)""",
    """cat=({category}[^=]+?)\s*\w+=""",
    """SECUDE\|C-Bus\|[^\|]+\|(|({activity_id}[^\|]+))\|(|(-|({event_name}[^\|]+)))\|"""
   
}
```