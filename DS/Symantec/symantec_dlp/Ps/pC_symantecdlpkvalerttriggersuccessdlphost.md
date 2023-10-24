#### Parser Content
```Java
{
Name = symantec-dlp-kv-alert-trigger-success-dlphost
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "MMM dd, yyyy HH:mm:ss"
  Conditions = ["""protocol=""","""policy=""","""rules=""" ,"""file_name=""","""dlp_host=""" ]
  Fields = [
    """ocurred_on=({time}.+)\s(PM|AM|am|pm|Am|Pm), reported""",
    """sender=(?!\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(N\/A|({email_address}[^,]+))""",
    """incident_id=({alert_id}\d+)""",
    """\sprotocol=({alert_type}[^,]+)""",
    """\spolicy=({alert_type}[^,]+)""",
    """\sseverity=({alert_severity}[^,]+)""",
    """\srules=({alert_name}[^,\)]+\)?)""",
    """\sdlp_host=({host}[^,]+)""",
    """blocked=({action}[^,]+)""",
    """recipients=({target}.+), severity=""",
    """file_name=({file_name}[^,]+)\s*""",
    """endpoint_machine_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """endpoint_user_id=({domain}[^\\]+)\\({user}[\w\.\-]{1,40}\$?)"""
   ]
   ParserVersion = "v1.0.0"


}
```