#### Parser Content
```Java
{
Name = unix-unix-cef-ssh-traffic-success-accepted
  Vendor = Unix
  Product = Unix
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """|Unix|Unix|""", """|Accepted""" ]
  Fields = [
    """\srt=({time}\d+)""",
    """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sduser=({user}.+?)\s+\w+=""",
    """\sdvc(host)?=({host}[^\s]+)""",
    """ dst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """ dhost=({dest_host}[^\s]+)""",
    """ cs4=({login_id}\d+)""",
    """\|Accepted ({auth}.+?)\|""",
    """({event_code}ssh)"""
  ]


}
```