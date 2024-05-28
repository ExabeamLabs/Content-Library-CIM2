#### Parser Content
```Java
{
Name = "pdns-recursor-json-dns-request-success-qname"
  Vendor = "PowerDNS"
  Product = "PowerDNS Recursor"
  TimeFormat = "epoch_sec"
  Conditions = [ """pdns-recursor""", """msg="""", """qname="""", """qtype="""" ]
  Fields = [
    """\Wts="({time}\d{10})"""
    """\s({host}[\w.-]+)\spdns-recursor"""
    """msg="({additional_info}[^"]+)"""
    """proto="({protocol}[^"]+)"""
    """qname="({dns_query}[^"]+)"""
    """qtype="({dns_query_type}[^"]+)"""
    """remote="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
    """source="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """subsystem="({log_source}[^"]+)"""
    """prio="({priority}[^"]+)"""
    """\Wtid="({thread_id}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```