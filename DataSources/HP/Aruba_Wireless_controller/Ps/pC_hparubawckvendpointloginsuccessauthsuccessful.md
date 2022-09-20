#### Parser Content
```Java
{
Name = hp-arubawc-kv-endpoint-login-success-authsuccessful
    Vendor = HP
    Product = Aruba Wireless controller
    TimeFormat = "MMM dd HH:mm:ss yyyy"
    Conditions = ["""User Authentication Successful: username=""", """AAA profile="""]
    Fields = [
      """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\+[^\s]+\s[^\s]+\s+\d+\s({host}[^\s]+)\sauthmgr\[({event_code}[^\]]+)\]""",
      """username=(({domain}[^\\\s\@]+)\\|({user_type}host)\/)?({email_address}[^\s\@]+\@({email_domain}[^\s]+))?({src_mac}([0-9a-fA-F]{1,2}[.:-]){5}([0-9a-fA-F]{1,2}))?({user}[^\s]+)?""",
      """IP=({dest_ip}[a-fA-F\d.:]+)""",
      """SSID=(N\/A|({network}[^\s]+))""",
      """\sauth server=({auth_server}[^\s]+)""",
   ]
   ParserVersion = "v1.0.0"
  

}
```