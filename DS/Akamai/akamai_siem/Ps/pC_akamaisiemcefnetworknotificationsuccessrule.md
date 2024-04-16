#### Parser Content
```Java
{
Name = akamai-siem-cef-network-notification-success-rule
   Vendor = Akamai 
   Product = Akamai SIEM
   TimeFormat = "epoch_sec"
   Conditions = [ """CEF:""", """Akamai|akamai_siem""", """requestMethod=""", """ cs2Label=Rule"""]
   Fields = [
    """start=({time}\d{10})""",
    """requestMethod=({method}[^=\s]+)""", 
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """cs2=({additional_info}[^,=]+?)(,|\s{0,100}\w+=)""",
    """act=({result}[^=]+)\s+\w+=""",
    """dhost=({web_domain}[^\s]+)\s+\w+=""",
    """request=({request_uri}[^\s]+)\s+\w+=""",
    """dpt=({src_port}\d+)""",
    """CEF:\d+\|([^\|]+\|){4}({event_name}[^\|]+)""", 
    """CEF:\d+\|([^\|]+\|){3}({category}[^\|]+)"""
   ]
   ParserVersion = v1.0.0


}
```