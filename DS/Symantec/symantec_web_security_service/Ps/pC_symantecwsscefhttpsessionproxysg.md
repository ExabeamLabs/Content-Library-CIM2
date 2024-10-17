#### Parser Content
```Java
{
Name = symantec-wss-cef-http-session-proxysg
  Vendor = Symantec
  Product = Symantec Web Security Service
  TimeFormat = "epoch"
  Conditions = [ """|Blue Coat|Proxy SG|""", """requestMethod=""" ]
  Fields = [
    """\srt=({time}\d{13})""",
    """\sdvc=({host}.+?)\s\w+=""",
    """\sdvchost="?({host}({src_host}[^\s"]+))""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s\w+=""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s\w+=""",
    """\sshost=({src_host}.+?)\s\w+=""",
    """\sdpt=({dest_port}\d+)\s\w+=""",
    """\ssuser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+=""",
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
    """\scn1=(-|({http_response_code}\d\d\d))""",
    """\|Blue Coat\|Proxy SG\|[^|]*\|({proxy_action}[^|]+)\|""",
    """requestContext=(?:-|({referrer}[^\s]+))""",
    """\scs4=(([^=]+?;)+)?(?:(none)|({category}.+?))\s+\w+="""
  ]
  DupFields = [ "user->orig_user" ]
  ParserVersion = "v1.0.0"


}
```