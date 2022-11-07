#### Parser Content
```Java
{
Name = cisco-umbrella-sk4-dns-response-success-allowed
  ParserVersion = v1.0.0
  Conditions = [ """destinationServiceName =Azure""", """dproc=Log Analytics OMS Workspace""", """"QueryType_s":"""", """"Action_s":"Allowed""""]

cef-cisco-dns-response-sk4-template {
  Vendor = Cisco
  Product = Cisco Umbrella
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """"ResponseCode_s":"({dns_response_code}[^"]+)"""
    """"Domain_s":"({dns_query}[^"]+)"""
    """"domain":"({dns_query}[^"]+)"""
    """"Action_s":"({action}[^"]+)"""
    """"QueryType_s":"({dns_query_type}[^"]+)"""
    """"Categories_s":"({categories}[^"]+)"""
    """"InternalIP_s":"({dest_ip}[^"]+)"""
    """"Identites_s":"([\w\s\.]+,)?(({full_name}\w+\s+\w+[^",]+?) \(({email_address}[^\)@]+?@[^\)]+?)\))?(,({dest_host}[^\(\)"\s]+))?"""
  
}
```