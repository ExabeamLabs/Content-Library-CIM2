#### Parser Content
```Java
{
Name = "microsoft-nps-xml-endpoint-authentication-packettype4-tl"
    Vendor = "Microsoft"
    Product = "Microsoft Network Policy Server"
    TimeFormat = "MM/dd/yyyy HH:mm:ss.SSS"
    Conditions = [
      "<packet-type data_type=\"0\">4</packet-type>"
      "<client-ip-address"
      "<computer-name"
    ]
    Fields = [
      "(?i)<Timestamp[^>]+>({time}\\d+\\/\\d+\\/\\d+\\s\\d+:\\d+:\\d+\\.\\d+)<"
      "(?i)<Computer-Name[^>]+>({host}[^<]+)<"
      "(?i)<User-Name[^>]+>(({email_address}[^@<]+@[^<]+)|(({domain}[^\\\\\\/<]+)[\\\\\\/]+)?({user}[^<]+))<"
      "(?i)<Client-IP-Address[^>]+>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)Proxy-Policy-Name[^>]+>({additional_info}[^<]+)<"
      "(?i)<Packet-Type[^>]+>({result}\\d+)"
      "(?i)<NAS-IP-Address data_type=[^>]+>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?<"
    ]
    DupFields = [
      "host->dest_host"
      "result->event_code"
    ]
    ParserVersion = "v1.0.0"
  

}
```