#### Parser Content
```Java
{
Name = cisco-cws-cef-http-session-requestmethod
    Vendor = Cisco
    Product = Cisco Cloud Web Security
    TimeFormat = "epoch"
    Conditions = [ """|CISCO|Cloud Web Security|""","""requestMethod="""]
    Fields = [
      """\srt=({time}\d{13})""",
      """\sagt=({host}[^\s]+)""",
      """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\srequest=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(:({dest_port}\d+))?""",
      """\ssrc=(?:0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
      """\sshost=(?:|({src_host}.+?))\s\w+=""",
      """\sduser=([^\s\\]+\\+)?(?:|UNDISCLOSED|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({user}[\w\.\-]{1,40}\$?))\s\w+=""",
      """\sact=(?:|({action}.+?))\s\w+=""",
      """\srequestMethod=(?:|({method}.+?))\s\w+=""",
      """\sout=({bytes_out}\d+)\s\w+=""",
      """\sin=({bytes_in}\d+)\s\w+=""",
      """\|CISCO\|Cloud Web Security\|[^|]*\|(?:0|({http_response_code}\d+))\|""",
      """\srequest=(?:-|({url}\S+))""",
      """\srequest=(?:-|(\w+:\/+)?({web_domain}[^:\/\s]+))""",
      """\srequest=(?:-|(({protocol}[^:]+))):\/""",
      """\srequest=(?:-|((\w+:\/+)?[^\/]+({uri_path}\/.*?)))(\?[^\s]*)?\srequestMethod=""",
      """\srequest=(?:-|((\w+:\/+)?[^?]*({uri_query}\?.*?)))\srequestMethod=""",
      """\srequestClientApplication=(?:-|({user_agent}.+?))\s\w+=""",
      """\scs2=(?:unclassified|({category}.+?))\s\w+=""",
      """\sfileType=(?:-|({mime}.+?))\s\w+=""",
    ]
	ParserVersion = "v1.0.0"
  

}
```