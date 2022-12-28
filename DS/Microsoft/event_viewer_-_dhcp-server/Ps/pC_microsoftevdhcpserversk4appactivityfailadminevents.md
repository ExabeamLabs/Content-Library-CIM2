#### Parser Content
```Java
{
Name = microsoft-evdhcpserver-sk4-app-activity-fail-adminevents
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """destinationServiceName =Azure""", """"Source":"Microsoft-Windows-DHCP-Server"""", """DNS operation refused""", """"EventLog":"DhcpAdminEvents"""" ]

cef-windows-dhcp-events = {
  Vendor = Microsoft
  Product = Event Viewer - DHCP-Server
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,7}Z)"""",
    """"Computer":"({host}[^"]+)"""",
    """"UserName":"(({domain}[^"\\]+)\\+)?({user}[^"]+)"""",
    """"operation\\?">({event_name}[^<]+?)\s*<\/Data>""",
    """EventID":({event_code}\d+)""",
    """Name\\?="Errorvalue">({error_code}\d+)""",
    """Name\\?="FQDNName">({dest_host}[^<]+)<\/Data>""",
    """Name\\?="IP_Name">\[{2}({dest_ip}[a-fA-F\d:.]+)\]{2}<\/Data>""",
    """"RenderedDescription":"({additional_info}[^"]+?)\s*""""
  
}
```