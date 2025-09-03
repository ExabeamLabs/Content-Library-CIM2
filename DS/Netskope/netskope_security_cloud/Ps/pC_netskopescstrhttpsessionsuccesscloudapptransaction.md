#### Parser Content
```Java
{
Name = "netskope-sc-str-http-session-success-cloudapptransaction"
Vendor = "Netskope"
Product = "Netskope Security Cloud"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [ """ http_transaction """, """ CloudApp """ ]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """\d\d:\d\d:\d\d\s+(?:-|\d+\s+){1}(?:-|({bytes_in}\d+))\s+(?:-|({bytes_out}\d+))\s+(?:-|({bytes}\d+))\s+(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+(?:-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s+(?:-|"*({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"*)\s+(?:-|({method}[^\s]+))\s+(?:-|({protocol}[^\s]+))\s+(?:-|({uri_query}[^\s]+))\s+(?:-|"*({user_agent}[^"]+)"*)\s+(?:-|"*(?:[^"]+)"*)\s+(?:-|({http_response_code}\d+))\s+(?:-|"*({mime}[^"]+("+[\w-]+)?)"*)\s+(?:-|({web_domain}[^\s]+))\s+(?:-|([^\s]+))\s+(?:-|({uri_path}[^&\?=,:\s]+)([^\s]*))\s+(?:-|\d+)\s+(?:-|"*({url}[^\s]+?)"*)\s+(?:-|\d+)\s+(?:-|"*([^"]+)"*)\s+(?:-|"*({app}[^"]+)"*)\s+(?:-|"*({country_code}[^"]+)"*)\s+(?:-|({remote_location_latitude}[^\s]+))\s+(?:-|({remote_location_longitude}[^\s]+))\s+(?:-|"*({location_city}[^"]+)"*)\s+(?:-|"*({location_state}[^"]+)"*)\s+"*(?:N\/A|-|[^\s]+?)"*\s+(?:-|"*({country}[^"]+)"*)\s+(?:-|[\d.-]+)\s+(?:-|[\d.-]+)\s+(?:-|"*[^"]+"*\s+){3}(?:-|"*({os}[^"]+)"*)\s+(?:-|"*({browser}[^"]+)"*\s+)(?:-|"*[^"]+?"*\s+){3}(?:-|\S+\s+){3}(?:[^"]+)"+(-|({category}[^"]+))"""",
  """(?:-|"({additional_info}[^"]+?)\s*")\s+http_transaction"""
]
ParserVersion = "v1.0.0"


}
```