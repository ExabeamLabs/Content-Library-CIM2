#### Parser Content
```Java
{
Name = "microsoft-evdnsserver-xml-network-notification-6004-tl"
    ParserVersion = "v1.0.0"
    Product = "Event Viewer - DNSServer"
    Conditions = [
      ">6004</eventid>"
      "dns_event_bad_zone_transfer_request"
      "<provider>microsoft-windows-dns-server-service</provider>"
      "<channel>dns server</channel>"
    ]
  

}
```