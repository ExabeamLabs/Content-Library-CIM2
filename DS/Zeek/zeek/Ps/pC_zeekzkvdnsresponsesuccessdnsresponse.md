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
  """ts="({time}\d{13})"""
  """id\.orig_h="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """id\.orig_p="({src_port}\d+)"""
  """id\.resp_h="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """id\.resp_p="({dest_port}\d+)"""
  """proto="({protocol}[^"]+)"""
  """trans_id="({query_id}\d+)"""
  """query="({dns_query}[^"\\]+)"""
  """qtype_name="({dns_query_type}[^"\\]+)"""
  """rejected="({result}[^"]+)"""
  """rcode="({rcode}[^"]+)"""
  """answers="({answers}[^"]+)"""
  """answers=({dns_response}.+?)\s\w+=(\s|")"""
]
ParserVersion = "v1.0.0"


}
```