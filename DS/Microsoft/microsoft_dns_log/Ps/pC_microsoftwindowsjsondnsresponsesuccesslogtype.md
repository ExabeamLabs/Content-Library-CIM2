#### Parser Content
```Java
{
Name = "microsoft-windows-json-dns-response-success-logtype"
ExtractionType = json
Vendor = "Microsoft"
Product = "Microsoft DNS Log"
TimeFormat = ["MM/dd/yyyy HH:mm:ss a", "MM/dd/yyyy hh:mm:ss a"]
Conditions = [
"""@timestamp":"""
""""log_type":"win_dns""""
""" R """
]
Fields = [
"""exa_json_path=$.host.name,exa_field_name=host"""
"""exa_regex=message\":\"({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+ (am|AM|pm|PM)) ({thread_id}\S+)\s+(\S+\s+){2}({protocol}\S+)\s+({operation}\S+)\s+(::1|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s+({query_id}\S+)\s+R \S+ \[\S+\s+(|({dns_query_flags}.+?))\s+({dns_response_code}\S+)\]\s+({dns_query_type}\S+)\s+({dns_query}[^\s\"\n]+?)(\\n)?\""""
]
ParserVersion = "v1.0.0"


}
```