#### Parser Content
```Java
{
Name = netskope-sc-cef-alert-trigger-success-dlp
  Vendor = "Netskope"
  Product = "Netskope Security Cloud"
  TimeFormat = "epoch_sec"
  Conditions = [ """CEF:0|Netskope|""", """|DLP|""" ]
  Fields = [
    """timestamp=({time}\d{10})""",
    """\|DLP\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|""",
    """({alert_type}DLP)""",
    """dlpFile=({file_name}[^=]+?)\s\w+=""",
    """dlpIncidentId=({alert_id}\d+?)\s""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """fsize=({bytes}\d+)\s"""
    """requestClientApplication=(null|({app}[^=]+?))\s\w+=""",
    """md5=({md5}[^=]+?)\s\w+=""",
    """sha256=({sha256}[^=]+?)\s\w+=""",
    """suser=(({email_address}[^@=\s]+@[^@=\s\.]+\.[^=\s]+)|({user}[^=@\\\/\s]+))""",
    """url=({target}[^~]+?)\s("|$)""",
  ]
  ParserVersion = v1.0.0


}
```