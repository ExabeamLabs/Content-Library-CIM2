#### Parser Content
```Java
{
Name = "symantec-bcpa-cef-app-notification-success-oktosenddata"
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|Blue Coat|Proxy SG|""", """catdt=Web Filtering""", """|Ok to send data|""" ]
  Fields = ${BlueCoatParserTemplates.cef-bluecoat-proxy.Fields}[
    """destinationServiceName =({app}ProxySG)"""
  ]

cef-bluecoat-proxy = {
  Vendor = Symantec
  Product = Symantec Web Security Service
  TimeFormat = "epoch"
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\|Blue Coat\|Proxy SG\|([^\|]*\|){2}({event_name}[^\|]+)""",
    """\Wmsg=({additional_info}.+?)(\s+\w+=|\s*$)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s""",
    """\Wagt=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
    """\Wdvchost=({host}[\w.-]+)""",
    """\Wahost=({src_host}[\w.-]+)""",
    """\Wdhost=({dest_host}[\w.-]+)""",
    """\Wcatdt=({event_category}.+?)(\s+\w+=|\s*$)""",
    """\WcategoryOutcome=\/?({result}[^\s]+)"""
  
}
```