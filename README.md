# Versions

- CAS `6.2.0`
- Java `15`

## Motivation

This project (as not-overlay) has the following benefits over overlay-template:
- Simple to use, and quick start (no more gradle commands)
- Fast
- Easy to debug
- Hot reloading

This project has also the following drawbacks:
- Changes to be made are more complex. Because, for changes to be made in the source code of CAS, our own custom classes and configurations to make these classes bean are required. As in the overlay template, the same package-class name structure doesn't work here.

## Start Up

The project is compiled and run by IDE. The following address is visited in the browser.
```bash
https://localhost:8443/cas/login
```

The default username and password is same as in cas-overlay-template.

```bash
username: casuser
password: Mellon
```

## Integration

If the CAS server is to be integrated with other projects in the development environment, the certificates/thekeystore.der public certificate under classpath must be imported into the jdk used.
```bash
keytool -import -alias thekeystore -storepass changeit -file thekeystore.der -keystore $JAVA_HOME\lib\security\cacerts
```