#### Parser Content
```Java
{
Name = "juniper-jn-kv-alert-trigger-success-idpattacklogevent"
Vendor = "Juniper Networks"
Product = "Juniper SRX Series"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """ - IDP_ATTACK_LOG_EVENT ["""
  """ message-type="""
  """ destination-interface-name=""""
]
Fields = [
  """ ({host}[^\s]+) [^\s]+ - IDP_ATTACK_LOG_EVENT """
  """({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\-\d\d:\d\d)\s"""
  """\ssource-address=\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
  """\ssource-port=\"({src_port}\d+)\""""
  """\sdestination-address=\"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\""""
  """\sdestination-port=\"({dest_port}\d+)\""""
  """\sprotocol-name=\"({protocol}[^\"]+)\""""
  """\sservice-name=\"({service_name}[^\"]+)\""""
  """\sapplication-name=\"({app}[^\"]+)\""""
  """\srule-name=\"({rule_id}[^\"]+)\""""
  """\saction=\"(NONE|({result}[^\"]+))\""""
  """\sthreat-severity=\"({alert_severity}[^\"]+)\""""
  """\sattack-name=\"({alert_name}[^\"]+)\""""
  """\susername=\"(N\/A|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\""""
  """\srulebase-name=\"({alert_type}[^\"]+)"""
]
ParserVersion = "v1.0.0"


}
```