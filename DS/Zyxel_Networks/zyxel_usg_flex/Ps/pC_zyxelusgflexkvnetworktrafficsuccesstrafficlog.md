#### Parser Content
```Java
{
Name = zyxel-usgflex-kv-network-traffic-success-trafficlog
  ParserVersion = "v1.0.0"
  Conditions = [ """ cat="Traffic Log"""", """ sourceTranslatedAddress="""", """ note="""", """ dir="""" ]
  Fields = ${ZyxelParsersTemplates.zyxel-network-events.Fields}[
    """\sproto="({protocol}[^"]+)""",
    """\sdir="({direction}[^"]+)""",
    """\ssent=({bytes_out}\d+)""",
    """\srcvd=({bytes_in}\d+)""",
    """\sduration=({duration}\d+)""",
    """\sclient_mac="({src_mac}[^"]+)""",
    """\ssourceTranslatedPort=(0|({src_translated_port}\d+))""",
    """\ssourceTranslatedAddress="({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""""  
  ]

zyxel-network-events = {
    Vendor = "Zyxel Networks"
    Product = "Zyxel USG FLEX"
    TimeFormat = ["MMM dd HH:mm:ss yyyy"]
    Fields = [
      """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)\s({host}[\w\-\.]+)\s"""
      """\suser="(?:unknown|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
      """\ssrc="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """\snote="({operation}[^"]+)"""
      """\smsg="({event_name}[^"]+)"""
      """\sdst="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """\sdevid="({devid}[^\s]+)"""",
      """\scat="({category}[^"]+)""",
    
}
```