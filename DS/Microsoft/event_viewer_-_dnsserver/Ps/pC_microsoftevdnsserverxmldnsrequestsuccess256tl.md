#### Parser Content
```Java
{
Name = "microsoft-evdnsserver-xml-dns-request-success-256-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - DNSServer"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<data name='qname'>"
      "<data name='qtype'>"
      "<data name='flags'>"
    ]
    Fields = [
      "(?i)TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d{9}Z)"
      "(?i)Computer>({host}.+?)<\\/Computer>"
      "(?i)EventID>({event_code}\\d+)<\\/EventID>"
      "(?i)Execution ProcessID='({process_id}\\d+)"
      "(?i)<Data Name ='XID'>({query_id}\\d+)"
      "(?i)ThreadID='({thread_id}[^\\']+)"
      "(?i)<Data Name ='InterfaceIP'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?"
      "(?i)<Data Name ='Source'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)<Data Name ='Port'>({src_port}\\d+)"
      "(?i)Name ='QNAME'>({dns_query}[^<]+)\\.?<\\/Data>"
      "(?i)<Data Name ='QTYPE'>({dns_query_type}.+?)<\\/Data>"
      "(?i)<Data Name ='Flags'>({dns_query_flags}.+?)<\\/Data>"
      "(?i)<Data Name ='BufferSize'>({bytes}\\d+)<\\/Data>"
    ]
    ParserVersion = "v1.0.0"
  

}
```