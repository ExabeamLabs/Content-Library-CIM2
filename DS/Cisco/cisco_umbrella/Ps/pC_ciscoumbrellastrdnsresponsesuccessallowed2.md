#### Parser Content
```Java
{
Name = cisco-umbrella-str-dns-response-success-allowed-2
  ParserVersion = "v1.0.0"
  Conditions = [""","33 (SRV)",""",""","Allowed","""]

cisco-dns-response = {
  Vendor = Cisco
  Product = Cisco Umbrella
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
     """(\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)(",("(({host}[\w.-]*)|[^,]*)"),"([^,]*,)?)(({full_name}[^"\(\)]+[\s,]+[^"\(\)]+?)?[\s\\\(]+\(((({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|\)]+)))|({user}[\w\.\-]{1,40}\$?)))[\s\\\)",]+"""
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)","({host}[^"]+)","[^,]+,({full_name}[^\(]+?)\s\(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^"]+\.[^"]+)\)","[^"]+","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","({result}Allowed)","({dns_query_type}[^"]+)","({dns_response_code}NOERROR|NXDOMAIN|SERVFAIL|REFUSED)","({dns_query}[^"]+)","(|({categories}({category}[^,"]+)[^"]*))""""
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)","[^"]+","[^,]+,"[^"]+","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","({result}Allowed)","({dns_query_type}[^"]+)","({dns_response_code}NOERROR|NXDOMAIN|SERVFAIL|REFUSED)","({dns_query}[^"]+)","(|({categories}({category}[^,"]+)[^"]*))""""
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)","[^"]+","[^,]+,({host}[\w\-.]+)","[^"]+","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","({result}Allowed)","({dns_query_type}[^"]+)","({dns_response_code}NOERROR|NXDOMAIN|SERVFAIL|REFUSED)","({dns_query}[^"]+)","(|({categories}({category}[^,"]+)[^"]*))"""",
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)","[^"]+","[^,]+,({host}[\w\-.]+)"?,"[^"]+","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","({result}Allowed)","({dns_query_type}[^"]+)","({dns_response_code}NOERROR|NXDOMAIN|SERVFAIL|REFUSED)","({dns_query}[^"]+)","(|({categories}({category}[^,"]+)[^"]*))""""
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)","[^"]+","[^,]+,({full_name}[^\(]+?)\s\(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^"]+\.[^"]+)\),({host}[^"]+)","[^"]+","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","({result}[^"]+)","({dns_query_type}[^"]+)","({dns_response_code}NOERROR|NXDOMAIN|SERVFAIL|REFUSED)","({dns_query}[^"]+)",""",
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)","[\w+\-.]+","({host}[\w\-.]+),"""
  
}
```