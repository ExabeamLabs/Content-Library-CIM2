#### Parser Content
```Java
{
Name = stealthbits-s-kv-endpoint-modify-objectmodified
  ParserVersion = "v1.0.0"
  Conditions = [ """StealthINTERCEPT""", """Object Modified""", """ObjectClass="computer"""", """ SuccessfulChange="""" ]
  Fields = ${StealthBitsParsersTempletes.stealthintercept-ad-events.Fields} [
    """\sDistinguishedName =\"({user_ou}[^\"]+)\""""
  ]


}
```