#### Parser Content
```Java
{
Name = silverfort-s-cef-app-login-adminconsole
  Vendor = Silverfort
  Product = Silverfort Authentication Platform
  TimeFormat =["dd/MM/yyyy HH:mm:ss.SSS","MM/dd/yyyy HH:mm:ss.SSS", epoch_sec]
  Conditions = [ """ CEF:""", """|Silverfort|Admin Console|""", """|Authentication|Authentication request|""" ]
  Fields = [
    """\s+({host}[\w\-.]+)\s+CEF:""",
    """rt=({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d.\d\d\d)""",
    """suser="?(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"?\ssntdom=""",
    """sntdom="?({domain}[^"]+)"\sshost""",
    """sntdom="?({domain}[^"]+)\sshost""",
    """shost="?(n\/a|({src_host}[\w\-\.]+))""",
    """src="?(n\/a|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """dhost="?(n\/a|({dest_host}[\w\-\.]+))""",
    """app="?(n\/a|({app}[^"]+))"?\scs1Label""",
    """cs2="?({action}[^"]+)"?\scs3Label""",
    """"rt="?({time}\d+)"""",
    """cs1="?({severity}[^"]+)"?\scs2Label""",
    """cs7="?({ioc}[^"]+)"?\scs8Label""",
    """cs4="?({policy_id}[^"]+)"?\scs5Label"""
    """cs5="?(n\/a|({result}[^"]+))"?\scs6Label"""
  ]
  ParserVersion = v1.0.0


}
```