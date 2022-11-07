#### Parser Content
```Java
{
Name = symantec-bcpa-cef-http-session-proxysg
  Vendor = Symantec
  Product = Symantec Blue Coat ProxySG Appliance
  TimeFormat = "epoch"
  Conditions = [ """|Blue Coat|Proxy SG|""", """requestMethod=""" ]
  Fields = [
    """\srt=({time}\d+)""",
    """\sdvc=({host}.+?)\s\w+=""",
    """\sdvchost=({host}[^\s]+)""",
    """\sdst=({dest_ip}.+?)\s\w+=""",
    """\ssrc=({src_ip}.+?)\s\w+=""",
    """\sshost=({src_host}.+?)\s\w+=""",
    """\sdpt=({dest_port}\d+)\s\w+=""",
    """\ssuser=({user}.+?)\s\w+=""",
    """\sact=({action}.+?)\s\w+=""",
    """\srequestMethod=({method}.+?)\s\w+=""",
    """\sout=({bytes_out}\d+)\s\w+=""",
    """\sin=({bytes_in}\d+)\s\w+=""",
    """\srequestProtocol=(?:-|({protocol}.+?))\s\w+=""",
    """\sdhost=(?:-|({web_domain}.+?))\s\w+=""",
    """\srequest=(?:(-|)|({url}.+?))\s\w+=""",
    """\srequestUrlFileName =(?:(-|)|({uri_path}.+?))\s\w+=""",
    """\srequestUrlQuery=(?:-|({uri_query}.+?))\s\w+=""",
    """\srequestClientApplication=(?:-|({user_agent}.+?))\s\w+=""",
    """\scat=(?:(none)|({category}.+?)(;.+?)?)\s+\w+=""",
    """\s(cs1|fileType)=(?:-|({mime}.+?)(;.+?)?)\s\w+=""",
    """\scn1=(?:-|({http_response_code}\d+)(;.+?)?)\s\w+=""",
    """\|Blue Coat\|Proxy SG\|[^|]*\|({proxy_action}[^|]+)\|""",
    """requestContext=(?:-|({referrer}[^\s]+))""",
  ]
  DupFields = [ "user->orig_user" ]
  ParserVersion = "v1.0.0"


}
```