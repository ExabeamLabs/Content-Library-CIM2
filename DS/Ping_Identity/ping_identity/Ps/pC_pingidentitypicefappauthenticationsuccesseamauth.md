#### Parser Content
```Java
{
Name = pingidentity-pi-cef-app-authentication-success-eamauth
  Conditions = [  """CEF:""", """|EAMAuth|""" ,"""|OAuth|""" ] 
  ParserVersion = "v1.0.0"

ping-auth-events{
   Vendor = Ping Identity
   Product = Ping Identity
   TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
   Fields = [
     """dvchost=({host}[^\s]+)""",
     """rt=({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d.\d\d\d)""",
     """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """msg=({result}[^\s]+)""",
     """cs3=\(\w+:({protocol}[^\s]+)\)""", 
     """cs5=({user}[^\s]+)""",
     """CEF:([^\|]*\|){3}({event_name}[^\|]+)\|""",
     """cs8=({user_agent}[^=]+?)\s+\w+=""",
     """cs7=(|({additional_info}[^\n]+?))\s+cs8Label="""
   ]   
},
}

LMSRuckusParserTemplates = {
exa-syslog-network-connection = {
  Vendor = Ruckus
  Product = Ruckus
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """User\s*\[({user}[\w.\-]+)(@({domain}[\w.\-]+))?(@({src_mac}(\w{2}:){5}\w{2}))?\]""",
    """User\s*\[({src_mac}(\w{2}:){5}\w{2})\]""",
    """User\s*\[host\/({src_host}[\w\-]+)(@({src_mac}(\w{2}:){5}\w{2}))?\]""",
    """WLAN\[({ssid}[^\]]+)""",
    """AP\[({wifiap}[^@\]]+)""",
  ]
  DupFields = [ "host->auth_server", "ssid->network", "wifiap->dest_host" 
}
```