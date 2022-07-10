### Transferir un dominio de una cuanta de AWS a otra cuenta.
```
# Ejecutar esto en la cuenta que tiene el dominio
> aws route53domains transfer-domain-to-another-aws-account --domain-name dominio.com --account-id <accountId>

# Una vez ejecutado arroja:
{
    "OperationId": "e9f30c8f-af43-4f9b-83e6-2f069fbf77ef",
    "Password": <password>
}

# Ejecutar esto en la cuenta que acepta el dominio
> aws route53domains accept-domain-transfer-from-another-aws-account --domain-name dominio.com --password <password> # Nota: el paword va entre comillas simples 'password'
```
