#### Parser Content
```Java
{
Name = "microsoft-evdnsserver-xml-network-notification-6522-tl"
    ParserVersion = "v1.0.0"
    Product = "Event Viewer - DNSServer"
    Conditions = [
      ">6522</eventid>"
      "dns_event_zone_transfer_in_progress"
      "<provider>microsoft-windows-dns-server-service</provider>"
      "<channel>dns server</channel>"
    ]
  

}
```