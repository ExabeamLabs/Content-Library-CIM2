#### Parser Content
```Java
{
Name = "microsoft-evdnsserver-xml-app-notification-3150-tl"
    ParserVersion = "v1.0.0"
    Product = "Event Viewer - DNSServer"
    Conditions = [
      ">3150</eventid>"
      "dns_event_zone_write_completed"
      "<provider>microsoft-windows-dns-server-service</provider>"
      "<channel>dns server</channel>"
    ]
  

}
```