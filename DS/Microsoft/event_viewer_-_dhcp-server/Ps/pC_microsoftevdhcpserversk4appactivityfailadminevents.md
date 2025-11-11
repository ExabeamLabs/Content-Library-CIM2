#### Parser Content
```Java
{
Name = microsoft-evdhcpserver-sk4-app-activity-fail-adminevents
  ParserVersion = "v1.0.0"
  Conditions = [ """"Source":"Microsoft-Windows-DHCP-Server"""", """DNS operation refused""", """"EventLog":"DhcpAdminEvents"""", """"EventID":""" ]
  Fields = ${DLWindowsParsersTemplates.cef-windows-dhcp-events.Fields}[
    """"UserName":"(({domain}[^"\\]+)\\+)?(({user}[\w\.\-\!\#\^\~]{1,40}\$?)"|({full_name}[^",]+))""",
    """Name\\?="IP_Name">\[{2}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\]{2}<\/Data>""",
    """"Computer":"({host}[^"]+)"""",
    """Name\\?="FQDNName">({dest_host}[\w\-.]+)<\/Data>"""
  ]

cef-windows-dhcp-events = {
  Vendor = Microsoft
  Product = Event Viewer - DHCP-Server
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,7}Z)"""",
    """"operation\\?">({event_name}[^<]+?)\s*<\/Data>""",
    """EventID":({event_code}\d+)""",
    """Name\\?="Errorvalue">({error_code}\d+)""",
    """"RenderedDescription":"({additional_info}[^"]+?)\s*""""
  
}
```