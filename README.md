
# Mail batch application

Un'applicazione Spring Batch di esempio per inviare e-mail a più destinatari. 
l'app ottine  gli indirizzi e-mail da un file CSV e invia un'e-mail a ciascun destinatario incluso un allegato. 
Un file csv di esempio e un file allegato sono forniti come esempi. 
Il codice utilizza il progetto [Spring Batch] (http://projects.spring.io/spring-batch/ "Spring Batch") per configurare un lavoro per questa attività.

 
## How to run the application

Java 8 is required. To run the application:

    mvn clean package
    java -jar target/mail-batch-0.0.1-SNAPSHOT.jar \
      --spring.mail.host=<host> \
      --spring.mail.port=<port> \
      --spring.mail.username=<user> \
      --spring.mail.password=<pass> \
      --codeurjc.batch.data=data.csv \
      --codeurjc.batch.attachment=sample-attachment.txt
    
## Release changes

**0.2.0** 

* Add velocity templates for building email subject and body

**0.1.0** 

* Initial implementation # mailSender
