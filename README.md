# hive-and-es6
Deploy TheHive Project (version 3) with the latest Elastic Search (version 6)

Certificate for TheHive Project

$ keytool -genkey -keyalg RSA -alias selfsigned -keystore thehivekeystore.jks -storepass passwd12 -validity 365 -keysize 4096

To Convert the above generated JKS certificate to PKCS12 certificate:
$keytool -importkeystore -srckeystore thehivekeystore.jks -srcstoretype JKS -deststoretype PKCS12 -destkeystore thehivekeystore.p12

Change the configuration in the application.conf as well as compose file while deployment.

NOTE: Please use only one of the Certificate, either JKS or PKCS12.
      And please change the password from "passwd12" to any other random one
      Also, the field play.http.secret.key="***thisisaninsecurepassword***" can be changed in the application.conf file
