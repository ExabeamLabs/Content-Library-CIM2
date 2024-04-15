#### Parser Content
```Java
{
Name = "microsoft-iis-xml-http-session-6200-tl"
    Vendor = "Microsoft"
    Product = "Microsoft IIS"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>6200</eventid>"
      "<provider name='microsoft-windows-iis-logging'"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d\\d\\d\\d\\d\\d\\dZ)'"
      "(?i)<Computer>({host}[^<]+?)<"
      "(?i)<Data Name ='cs-method'>(-|({method}[^<]+?))<"
      "(?i)<Data Name ='sc-status'>(-|({http_response_code}\\d+))<"
      "(?i)<Data Name ='cs-uri-stem'>(-|\\/|({uri_path}[^<]+?))<"
      "(?i)<Data Name ='cs-uri-query'>(-|({uri_query}[^<]+?))<"
      "(?i)<Data Name ='c-ip'>(::1|127.0.0.1|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?)<"
      "(?i)<Data Name ='s-ip'>(::1|127.0.0.1|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?)<"
      "(?i)<Data Name ='s-port'>(-|({dest_port}\\d+?))<"
      "(?i)<Data Name ='sc-bytes'>({bytes_out}\\d+)"
      "(?i)<Data Name ='cs-bytes'>({bytes_in}\\d+)"
      "(?i)<Data Name ='csUser-Agent'>(-|({user_agent}[^<]+?))<"
      "(?i)<Data Name ='cs-host'>(-|({web_domain}[^<]+?))<"
      "(?i)<Keywords>({result}[^<]+)<"
      "(?i)<Data Name ='s-computername'>(-|({src_host}[^<]+?))<"
      "(?i)<Data Name ='cs-username'>(-|(0#\\.f\\|ww\\|)?({user}[^@.<]+)@({domain}[^.\\d<]+)?)<"
      "(?i)<Data Name ='cs-username'>(-|((0#\\.f\\|ww\\|)|(0#\\.w\\|))?(((({domain}[^\\\\]+)\\\\)?({user}[^@<]+?))|({email_address}[^@]+@[^.<]+?\\.[^<]+)))<"
    ]
    ParserVersion = "v1.0.0"
  

}
```