#### Parser Content
```Java
{
Name = stealthbits-s-kv-user-modify-objectmodified
  ParserVersion = "v1.0.0"
  Conditions = [ """StealthINTERCEPT""", """Object Modified""", """ObjectClass="user"""", """ SuccessfulChange="""" ]
  Fields = ${StealthBitsParsersTempletes.stealthintercept-ad-events.Fields} [
    """\sDistinguishedName =\"({user_ou}[^\"]+)\""""
  ]


}
```