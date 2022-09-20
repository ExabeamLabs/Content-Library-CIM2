#### Parser Content
```Java
{
Name = zeek-z-str-dns-response-success-dnslog
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ 
"""/dns.log"""
]
  Fields = [
    """({time}\d{10})\.\d{6}\s+({user_uid}[^\s]+)\s+(({id_orig_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+)\s+(({id_orig_p}\d+?)|[^\s]+)\s+(({id_resp_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+)\s+(({id_resp_p}\d+?)|[^\s]+)\s+({protocol}[^\s]+)\s+({trans_id}[^\s]+)\s+({rtt}[^\s]+)\s+({query}[^\s]+)\s+({qclass}[^\s]+)\s+({qclass_name}[^\s]+)\s+({qtype}[^\s]+)\s+({qtype_name}[^\s]+)\s+({rcode}[^\s]+)\s+({rcode_name}[^\s]+)\s+({AA}[^\s]+)\s+({TC}[^\s]+)\s+({RD}[^\s]+)\s+({RA}[^\s]+)\s+({Z}[^\s]+)\s+({dns_response}[^\s]+)\s+({TTLs}[^\s]+)\s+({rejected}[^\s]+?)\s*$""",
    """\d{10}\.\d{6}\s+([^\s]+\s+){14}(?:-|({dns_response_code}[^\s]+))\s"""
  ]
  DupFields = [ "id_orig_h->src_ip", "id_orig_p->src_port", "id_resp_h->dest_ip", "id_resp_p->dest_port", "qtype->dns_query_type", "rejected->action" ]


}
```