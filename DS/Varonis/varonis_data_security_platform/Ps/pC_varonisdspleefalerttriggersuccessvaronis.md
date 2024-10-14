#### Parser Content
```Java
{
Name = varonis-dsp-leef-alert-trigger-success-varonis
  Vendor = Varonis
  Product = Varonis Data Security Platform
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """LEEF:""", """|Varonis|DatAdvantage|""", """Event_Type=""" ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}\S+)\s+LEEF""",
    """devTime=({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """accountName =({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)""",
    """domain=(|({domain}[^=]+))\s+(\w+=|$)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+(\w+=|$)""",
    """Event_Type=({event_name}[^=]+)\s+(\w+=|$)""",
    """Event_Status=({action}[^=]+)\s+(\w+=|$)""",
    """cat=({alert_type}[^=]+?)\s+(\w+=|$)""",
    """DatAdvantage\|[^\\]+?\|({alert_name}[^\\]+?)\|""",
    """sev=({alert_severity}\d+)""",
    """usrName =(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)""",
    """Alert_Description=({additional_info}[^=]+?)\s+(\w+=|$)"""
  ]


}
```