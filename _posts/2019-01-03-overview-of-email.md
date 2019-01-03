---
layout: post
title:  "Overview of Email"
date:   2019-01-3 12:00:00 +0530
categories: jekyll update
---
Electronic mail or E-mail is one the oldest and commonly used digital medium of communication. This article will focus on behind the scenes working of email. If you want to know about the history, evolution, features, rules and etiquettes associated with E-mail, look elsewhere.

The email system is based on the postal system, where an Authoritative Entity (AE) handles the receiving, routing and dispatching of mail. In the electronic space these authoritative entities could be public or private mail hosting providers unlike the physical world were the postal department is a government entity.  A better understanding of the roles and responsibilities can be achieved via an example.

Consider one to be the AE for the domain emailhost.com. In order for our customers to receive mails from the outside world, we need to create an MX (Mail Exchanger) record which associates the domain to our AE server IP address. Once the MX record is setup and distributed via your favorite DNS provider, we can start receiving emails for the domain emailhost.com. The emails received are scrutinized for spam, viruses and other nasty stuff before its delivered to the appropriate destination mailbox. Routing of the user's email to the appropriate storage location is completely handled by the AE. Similarly, if the customer wishes to send out an email the authoritative entity performs a series of checks and tests before sending the email to the target domain's AE. 
 
