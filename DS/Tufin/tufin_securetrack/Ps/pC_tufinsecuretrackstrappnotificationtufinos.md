#### Parser Content
```Java
{
Name = tufin-securetrack-str-app-notification-tufinos
 Product = Tufin SecureTrack
 Vendor = Tufin
 TimeFormat = "yyyy-MM-dd HH:mm:ss"
 ParserVersion = "v1.0.0"
 Conditions = [ """ELM""", """Tufin SecureTrack""", """Server TufinOS""" ]
 Fields =[
    """TufinOS\(({dest_host}[^\s:]+)\):\s+({src_host}[^\s]+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\(\d+\):*"*\s+({event_name}.+)\s"""
   ]
   DupFields = ["dest_host->host"]


}
```