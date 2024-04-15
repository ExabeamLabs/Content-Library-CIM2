#### Parser Content
```Java
{
Name = "absolute-siemconnector-cef-alert-trigger-success-absolute"
Vendor = "Absolute"
Product = "Absolute SIEM Connector"
TimeFormat = "MMM dd yyyy HH:mm:ss z"
Conditions = [
"""CEF:"""
"""|Absolute|AbsoluteSIEMConnector|"""
"""|Absolute.System.Alerts|"""
]
Fields = [
"""\Wrt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d \w+)"""
"""({host}[\w.\-]+)\s+CTAlertEvents"""
"""CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
"""\Wdhost=(|({dest_host}.+?))(\s+\w+=|\s*$)"""
"""\Wcn1=(|({alert_id}.+?))(\s+\w+=|\s*$)"""
"""\Wmsg=(|({additional_info}.+?))(\s+\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```