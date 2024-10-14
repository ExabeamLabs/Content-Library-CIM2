#### Parser Content
```Java
{
Name = axway-gateway-str-endpoint-login-success-edge
  Vendor = Axway
  Product = Axway Gateway
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """edge_source=""", """edge_host=""", """edge_fleet=""", """Axway""" ]
  Fields = [
    """edge_source="({additional_info}[^=]+?)"\s+\w+"""
    """edge_host="({host}[^=]+?)"\s+\w+"""
    """edge_fleet="({group_name}[^=]+?)"\s+\w+"""
    """({time}\d+-\d+-\d+\s\d+:\d+:\d+)"""
    """\s({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s"""
    """\s({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s\d+\s+({file_path}.+?)\s({category}[a-z])\s+({secured}[a-z])\s+({edge_response_status}[a-z])\s+({access_type}[a-z])\s+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|'\\_]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+({server_name}[^\s]+)\s"""
  ]
  ParserVersion = "v1.0.0"  


}
```