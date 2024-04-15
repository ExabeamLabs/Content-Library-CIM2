#### Parser Content
```Java
{
Name = "microsoft-evdnsserver-xml-dns-traffic-fail-5502-tl"
    Product = "Event Viewer - DNSServer"
    ParserVersion = "v1.0.0"
    Conditions = [
      ">5502</eventid>"
      "dns_event_bad_tcp_message"
      "<channel>dns server</channel>"
    ]
  

}
```