#### Parser Content
```Java
{
Name = "zeek-z-json-dns-request-success-uid"
Vendor = "Zeek"
Product = "Zeek"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
""""dns.log""""
""""uid":""""
""""id.orig_h":""""
""""id.resp_h":""""
""""query":""""
]
Fields = [
""""HOST"+:\s*\"+({host}[^\"]+)""""
""""TAGS"+:\s*\"+({event_code}[^\"]+)""""
""""ts\\?\"+:\\?\"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""""
""""id\.orig_h\\?\"+:\\?\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""id\.orig_p\\?\"+:({src_port}\d+)""""
""""id\.resp_h\\?\"+:\\?\"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
""""id\.resp_p\\?\"+:({dest_port}\d+)""""
""""proto\\?\"+:\\?\"+({protocol}[^\"\\]+)""""
""""trans_id\\?\"+:({query_id}\d+)""""
""""query\\?\"+:\\?\"+({dns_query}[^\"\\]+)""""
""""qtype_name\\?\"+:\\?\"+({dns_query_type}[^\"\\]+)""""
""""rejected\\?\"+:({result}\w+)""""
]
ParserVersion = "v1.0.0"


}
```