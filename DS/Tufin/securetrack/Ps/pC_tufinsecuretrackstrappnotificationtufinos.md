#### Parser Content
```Java
{
Name = tufin-securetrack-str-app-notification-tufinos
 Product = SecureTrack
 Vendor = Tufin
 TimeFormat = "yyyy-MM-dd HH:mm:ss"
 ParserVersion = "v1.0.0"
 Conditions = [ """ELM""", """Tufin SecureTrack""", """Server TufinOS""" ]
 Fields =[
    """TufinOS\(({dest_host}[^\s:]+)\):\s+({src_host}[^\s]+)\s+({src_ip}[a-zA-Z0-9.:]+)\s+\(\d+\):*"*\s+({event_name}.+)\s"""
   ]
   DupFields = ["dest_host->host"]


}
```