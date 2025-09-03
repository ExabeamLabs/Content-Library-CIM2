#### Parser Content
```Java
{
Name = cisco-umbrella-str-dns-response-success-allowed-3
  ParserVersion = "v1.0.0"
  Conditions = [""","48 (DNSKEY)",""",""","Allowed","""]

cisco-dns-response = {
  Vendor = Cisco
  Product = Cisco Cloud Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)",("[^"]*?",|[^,]*?,){2}"(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)","(|({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_translated_port}\d+))?)",(|("[^"]*",))"(|({result}[^",]+))","({dns_query_type}[^"]+)","({dns_response_code}NOERROR|NXDOMAIN|SERVFAIL|REFUSED)","({dns_query}[^"]+)",("[^"]*?",|[^,]*?,)"(|({categories}({category}[^,"]+)[^"]*))""""
    """(\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)(",("(({host}[\w.-]*)|[^,]*)"),"([^,]*,)?)(({full_name}[^"\(\)]+[\s,]+[^"\(\)]+?)?[\s\\\(]+\(((({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|\)]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))[\s\\\)",]+"""
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)","({host}[^"]+)","[^,]+,({full_name}[^\(]+?)\s\(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^"]+\.[^"]+)\)","[^"]+","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","({result}Allowed)","({dns_query_type}[^"]+)","({dns_response_code}NOERROR|NXDOMAIN|SERVFAIL|REFUSED)","({dns_query}[^"]+)","(|({categories}({category}[^,"]+)[^"]*))""""
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)","[^"]+","[^,]+,"[^"]+","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","({result}Allowed)","({dns_query_type}[^"]+)","({dns_response_code}NOERROR|NXDOMAIN|SERVFAIL|REFUSED)","({dns_query}[^"]+)","(|({categories}({category}[^,"]+)[^"]*))""""
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)","[^"]+","[^,]+,({host}[\w\-.]+)","[^"]+","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","({result}Allowed)","({dns_query_type}[^"]+)","({dns_response_code}NOERROR|NXDOMAIN|SERVFAIL|REFUSED)","({dns_query}[^"]+)","(|({categories}({category}[^,"]+)[^"]*))"""",
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)","[^"]+","[^,]+,({host}[\w\-.]+)"?,"[^"]+","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","({result}Allowed)","({dns_query_type}[^"]+)","({dns_response_code}NOERROR|NXDOMAIN|SERVFAIL|REFUSED)","({dns_query}[^"]+)","(|({categories}({category}[^,"]+)[^"]*))""""
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)(",("[^"]*"),"([^,]*,)?)({full_name}[^\(]+?)\s\(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^"]+\.[^"]+)\),({host}[\w.-]+)\s*(\(\d+\))?","[^"]+","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","({result}[^"]+)","({dns_query_type}[^"]+)","({dns_response_code}NOERROR|NXDOMAIN|SERVFAIL|REFUSED)","({dns_query}[^"]+)",""",
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)","[\w+\-.]+","({host}[\w\-.]+),"""
  
}
```