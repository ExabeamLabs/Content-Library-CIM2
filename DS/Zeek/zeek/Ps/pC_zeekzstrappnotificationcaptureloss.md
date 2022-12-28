#### Parser Content
```Java
{
Name = zeek-z-str-app-notification-captureloss
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """/capture_loss.log""" ]
  Fields = [
    """({time}\d{10})\.\d{6}\s+"""
# acks is removed
]
  DupFields = [ "peer->src_interface" ]
  ParserVersion = "v1.0.0"


}
```