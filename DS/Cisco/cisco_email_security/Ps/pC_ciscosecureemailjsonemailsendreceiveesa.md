#### Parser Content
```Java
{
Name = cisco-secureemail-json-email-send-receive-esa
  Vendor = Cisco
  Product = Cisco Email Security
  TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
  Conditions = [ """ ESAMailFlowPolicy=""", """ ESAURLDetails=""", """ duser=""", """ ESAMsgSize=""" ]
  Fields = [
    """\sstart=({time}\w{3}\s\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d{4})\s""",
    """\ssuser=({email_address}[^@]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """\sduser=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s""",
    """\sact=({action}[^\s]+)\s""",
    """\sESAMsgSize=({bytes}\d+)""",
    """\sdeviceDirection=({direction}[^=]+)\s\w+=""",
    """\scs4='({message_id}[^']+)'""",
    """\sshost=({src_host}[\w\-.]+)\s""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
    """\smsg='({email_subject}[^']+)'\s""",
    """\scs1=({policy_name}[^=]+)\s\w+="""
  ]
  ParserVersion = v1.0.0


}
```