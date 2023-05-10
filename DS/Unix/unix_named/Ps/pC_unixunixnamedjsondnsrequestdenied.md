#### Parser Content
```Java
{
Name = unix-unixnamed-json-dns-request-denied
  Conditions = [ """"message":"""", """ query (cache) """, """ denied """ ]
  Fields = ${BINDParserTemplates.bind-events.Fields} [
    """"message":"client ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})#({src_port}\d+)\s+\((|({dns_query}(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|([^\(\)]+))).*?\):\s*query \(cache\) \'({=query}(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|([^\s\/']+))(\/({dns_query_type}[^\s\/']+)\/({dns_query_flags}[^\s\/']+))'""",
    """({action}denied)""",
  ]
  ParserVersion = "v1.0.0"

bind-events = {
  Vendor = Unix
  Product = Unix Named
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"@timestamp":"({time}[^"]+)""",
    """"severity":({severity}[^",]+)""",
    """"priority":({priority}[^",]+)""",
    """"hostname":"({host}[^",]+)""",
    """"source":"({log_source}[^",]+)""",
    """"source":"[^"]*?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"message":"[^"]*?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\#({src_port}\d+)""",
    """"message":"({additional_info}[^"]+?)\s*"""",
  
}
```