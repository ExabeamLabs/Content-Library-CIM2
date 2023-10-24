#### Parser Content
```Java
{
Name = "catonetworks-cc-json-vpn-http-success-sdp"
Conditions = [
  """"event_sub_type":""""
  """"action":"SDP """
  """"event_type":"Security""""
]
ParserVersion = "v1.0.0"

json-catonetwork = {
  Vendor = "CatoNetworks"
  Product = "Cato Cloud"
  TimeFormat = "epoch"
  Fields = [
    """"time":({time}\d{13})""",
    """"src_country":"({src_country}[^="]+)"""",
    """"dest_country":"({dest_country}[^="]+)"""",
    """dest_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dest_port":({dest_port}\d+)""",
    """src_port":({src_port}\d+)""",
    """"categories":\["({categories}[^",;\]=]+)"""",
    """"action":"({action}[^="]+)"""",
    """"domain_name":"({domain}[^"=,]+)"""",
    """host_name":"({host}[^",]+)""""
    """user_email":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
    """"event_type":\s*"({event_category}[^",]+)""""
    """"event_sub_type":\s*"({sub_category}[^",]+)""""
  
}
```