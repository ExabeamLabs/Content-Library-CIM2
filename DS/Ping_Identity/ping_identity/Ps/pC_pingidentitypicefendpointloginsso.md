#### Parser Content
```Java
{
Name = pingidentity-pi-cef-endpoint-login-sso
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
  Conditions= [ """CEF:""", """|GlobalAuth|SSAA|""", """responsetime=""" ]
  Fields=[
    """CEF:([^\|]*\|){3}(|({auth_method}[^\|]+))\|(|({protocol}[^\|]+))\|""",
    """\Wrt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d+)""",
    """\Wcs3=\(({role}[^=:]+?):({protocol}[^=:]+?)\)""",
    """\Wresponsetime=({response_size}\d+)""",
    """\Wduid=(|({email_subject}.+?))(\s+\w+=|\s*$)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wmsg=(|({result}.+?))(\s+\w+=|\s*$)""",
    """\Wcs1=(|({app}.+?))(\s+\w+=|\s*$)""",
    """\Wcs2=(|({connection_id}.+?))(\s+\w+=|\s*$)""",
    """\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)""",
    """\Wcs4=(|({adopter_id}.+?))(\s+\w+=|\s*$)""",
    """\WexternalId=(|tid:({tracking_id}.+?))(\s+\w+=|\s*$)""",
    """\Wcs5=(|({local_user_id}.+?))(\s+\w+=|\s*$)""",
    """\Wcs6=(|({attributes}.+?))(\s+\w+=|\s*$)""",
    """\WSAML_SUBJECT\\=(|({email_address}[^=@]+?@[^=@]+?),?|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+\\=|\s*$)""",
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "auth_method->operation" ]


}
```