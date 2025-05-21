#### Parser Content
```Java
{
Name = forcepoint-wsg-cef-http-session-request
  ParserVersion = v1.0.0
  Vendor = Forcepoint
  Product = Websense Security Gateway
  TimeFormat = ["epoch", "epoch_sec"]
  Conditions = [ 
"""CEF"""
"""|Forcepoint|"""
""" app=""" 
""" request=""" 
]
  Fields = [
    """\srt=({time}\d{10,13})""",
    """\sdvc=(-|({host}[^\s]+))""",
    """\sdvchost=({host}[^\s]+)""",
    """\sshost=({src_host}[^\s]+)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sspt=({src_port}\d+)""",
    """\sdpt=({dest_port}\d+)""",
    """\ssuser=(-|(?:\w+:\/+[^=]+)\s+({user_ou}[^\/]+)\/({full_name}[^=]+?))\s+\w+=""",
    """\sact=({action}[^=]+?)\s\w+=""",
    """\srequestMethod=(?:-|({method}[^=]+?))\s\w+=""",
    """\sin=({bytes_in}\d+)""",
    """\sout=({bytes_out}\d+)""",
    """\sapp=(?:-|({protocol}[^=]+?))\s\w+=""",
    """\srequestProtocol=(?:-|({protocol}[^=]+?))\s\w+=""",
    """\sdhost=(?:|({web_domain}[^=]+?))\s\w+=""",
    """\srequest=({url}\S+)""",
    """\srequest=(?:-|(\w+:\/+[^\/]+({uri_path}\/[^\s\?]+)({uri_query}\?[^\s]+)?))(\s+\w+=|$)""",
    """\srequestUrlFileName =(?:|({uri_path}[^=]+?))\s\w+=""",
    """\srequestUrlQuery=(?:|({uri_query}[^=]+?))\s\w+=""",
    """\srequestClientApplication=(?:-|({user_agent}[^=]+?))\s+(\w+=|$)""",
    """CEF:([^\|]+\|){4}(\d+|({category}[^\|]+))\|""",
    """CEF:([^\|]+\|){4}(|({category_id}\d+))\|""",
    """\scs4=({category}[^=]+?)(\s+\w+=|;)""",
    """\scs5=({sub_category}[^=]+?)(\s+\w+=|;)""",
    """\sflexString1=(?:User Defined[^=]+?|({category}[^=]+?))\s+\w+=""",
    """\sflexString2=(?:User Defined.+?|({sub_category}.+?))\s+\w+=""",
    """\scs3=(?:-|({mime}[^=]+?))(\s+\w+=|;)""",
    """suser=(-|({last_name}[^,]+),\s({first_name}([A-Za-z]+){1}(\s\w){0,1}))\s""",
    """suser=\w+:\/+([^\s]+)?\s*((CN|OU)\\+=[^,]+,){1,2}DC\\=[^,]+,DC\\=[^\/]+\/({full_name}({last_name}[^\\]+)\\+,\s*({first_name}[^=]*?))\s\w+=""",
    """loginID=(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  ]


}
```