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
    """\srt=({time}\d{13})""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sduser=({user}.+?)\s+\w+=""",
    """\sdvc(host)?=({host}[^\s]+)""",
    """ dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """ dhost=({dest_host}[^\s]+)""",
    """ cs4=({login_id}\d+)""",
    """\|Accepted ({auth}.+?)\|""",
    """({event_code}ssh)"""
  ]


}
```