#### Parser Content
```Java
{
Name = zeek-z-kv-dns-response-success-dnsresponse
Vendor = Zeek
Product = Zeek
TimeFormat = "epoch"
Conditions = [
  """id.orig_h=""""
  """id.resp_h=""""
  """query=""""
  """qtype_name="""
]
Fields = [
  """ts="({time}\d+)"""
  """id\.orig_h="({src_ip}[a-fA-F\d.:]+)"""
  """id\.orig_p="({src_port}\d+)"""
  """id\.resp_h="({dest_ip}[a-fA-F\d.:]+)"""
  """id\.resp_p="({dest_port}\d+)"""
  """proto="({protocol}[^"]+)"""
  """trans_id="({query_id}\d+)"""
  """query="({dns_query}[^"\\]+)"""
  """qtype_name="({dns_query_type}[^"\\]+)"""
  """rejected="({result}[^"]+)"""
  """rcode="({rcode}[^"]+)"""
  """answers="({dns_response}[^"]+)"""
  """answers=({dns_response}.+?)\s\w+=(\s|")"""
]
ParserVersion = "v1.0.0"


}
```