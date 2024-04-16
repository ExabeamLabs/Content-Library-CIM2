#### Parser Content
```Java
{
Name = "pingidentity-pi-json-vpn-authentication-success-pingid"
Conditions = [
""""source":"PINGID""""
""""type":"user""""
""""status":"POLICY""""
""""message":"""
""""resources":"""
""""result":{"""
]
ParserVersion = "v1.0.0"

s-ping-events = {
  Vendor = Ping Identity
  Product = Ping Identity
  ExtractionType = json
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
  Fields = [
    """exa_json_path=$.Time,exa_field_name=time"""
    """exa_json_path=$.duid,exa_regex=(({domain}[^"@\\\/]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?)"""
    """exa_json_path=$.duid,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
    """exa_json_path=$.SRCIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$..remoteAddr,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.Status,exa_field_name=result"""
    """exa_json_path=$.Protocol,exa_field_name=protocol"""
    """exa_json_path=$.PingHost,exa_field_name=host"""
    """exa_json_path=$.EventType,exa_field_name=operation"""
    """exa_json_path=$.DescriptionFail,exa_field_name=failure_reason"""
  
}
```