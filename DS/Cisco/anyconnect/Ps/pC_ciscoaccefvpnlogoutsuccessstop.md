#### Parser Content
```Java
{
Name = cisco-ac-cef-vpn-logout-success-stop
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = AnyConnect
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """cisco-av-pair=mdm-tlv=ac-user-agent=AnyConnect""", """Acct-Status-Type=Stop""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}[^\s]+)""",
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d)""",
    """UserName =(({email_adress}[^@,]+@[^,]+)|(({domain}[^\\,]+)\\+)?({user}[^,]+))""",
    """Device\sIP\sAddress=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """NetworkDeviceName =({src_host}[^,]+)""",
    """NAS-IP-Address=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Calling-Station-ID=(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({src_host}[\w\-\.]+)),""",
    """NAS-Port=({dest_port}\d{1,9})\D""",
    """Acct-Session-Time=({session_duration}[^,]+)""",
    """Acct-Terminate-Cause=({reason}[^,]+)"""
  ]


}
```