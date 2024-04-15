#### Parser Content
```Java
{
Name = "cisco-ise-kv-configuration-modify-success-52001"
  Conditions = [
    """CISE_Administrative_and_Operational_Audit"""
    """ 52001 """
    """Changed configuration"""
  ]
  ParserVersion = "v1.0.0"

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
    """"InternalIP_s":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """"Identites_s":"([\w\s\.]+,)?(({full_name}\w+\s+\w+[^",]+?) \(({email_address}[^\)@]+?@[^\)]+?)\))?(,({dest_host}[^\(\)"\s]+))?"""
  
}
```