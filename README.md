Introducere în AngularJS
========================

![logo](img/AngularJS-large.png)

Radu Potop

--------------------------

AngularJS
=========

A Javascript MVC framework

* two way data binding
* modules
* directives
* testing
* makes large apps maintainable

--------------------------

WAT??
=====

![scratch head pic](img/consumer-reports-discovers-problem-with-the-ipad.jpg)

Cum am ajuns aici?
==================

--------------------------

Un pic de istorie
-----------------

![](img/1.png)

* La inceput: give me a doc!

--------------------------

![](img/4.png)

* Give me a fragment!

--------------------------

* Evolutia pe server-side: Scripts -> Frameworks MVC
* HTML -> JSON
* still using jQuery

![](img/5.png)

--------------------------

* Dropped Views pe server-side

![](img/7.png)

Code to assemble page (jQuery) -> Javascript MVC Framework

--------------------------

--------------------------

AngularJS
=========

A Javascript MVC framework

* two way data binding
* routing
* modules
* templates
* directives
* testing
* makes large apps maintainable

--------------------------

MVC
===

* explain MVC

* A lot more than Model - View - Controller
* HTML enhanced for web apps!
* AngularJS lets you extend HTML vocabulary for your application.

--------------------------

Routing
=======

* explain

--------------------------

Two way data binding
====================

Modificarile din model se propaga instant in view, si invers.

Model <---> View

* Mode in sync with the View.
* Scope = an object that wires up the model and view
* scope are anumite metode, like $eval

--------------------------

Modules / Servicii
==================

Unitati care incapsuleaza o functionalitate bine definita / clase

Servicii
--------

* chart
* pagination
* etc

Many built-in services
----------------------

* xhr, resource, route, location, 

--------------------------

Dependency Injection
====================

* Serviciile sunt injected in controllere
* Pot fi mocked pentru testare

--------------------------

Directive
=========

* Augmenteaza codul HTML prin elemente sau atribute definite de catre developer.
* Manipularea de DOM se realizeaza in interiorul directivelor
* pentru a nu avea DOM manip in controllere si in tot codul.

--------------------------

Templates
=========

* {{phone.name}}
* ng-repeat=””
* filtre
* etc.

Declarative is better than procedural

--------------------------

Cum funcționează împreună?
==========================

* bootstrapped printr-o directiva/un atribut special
* sunt lansate serviciile
* sunt pornite controllerele in functie de ruta curentă
* sunt compilate templates/views care conțin directivele
* se face two way data binding intre modele si views prin intermediul scope


--------------------------

--------------------------

Case study: Sendmachine
========================

![sendmachine](img/sm.png)

Ce are special Sendmachine?

--------------------------

ACL service + Session service
=============================

* permite accesul pe routes in functie de credentiale/grup

Grupuri:

* guest
* new
* confirmed
* expired

* in caz de 401 pe orice resursa esti scos din aplicatie

--------------------------

Form Validation service
=======================

* rulează **aceleași** reguli atât pe front-end cat si pe back-end
* regulile folosite de backend pentru validare sunt expuse printr-un API RESTful si refolosite de catre front-end pentru validarea forms
* chained rules:
	* required | valid_email | existing_email

--------------------------

Storage + Request Cache
=======================

* stocheaza în local storage datele dintr-un form
* in cazul unui 401, 403 sa poti recupera datele introduse

--------------------------

Lang service
============

* Localizare
* limba + locale poate fi schimbata on the fly

--------------------------

Permalink service
=================

* Deeplink
* linkuire la o anumita stare a aplicatiei

--------------------------

Chart service
=============

* wraps Highcharts
* timeseries pe luni / zile / ore
* polling
* getPeriod: today, last_24_hours, yesterday, last_30_days

![](img/chart.png)

--------------------------

Directives
==========

* pagination
* editor (ACE)

	code here

--------------------------

Filters
=======

* date (locale aware)
* numbers (locale aware)

--------------------------

So why use AngularJS?
=====================

* makes large apps maintainable
* less DOM manipulation

--------------------------

More
====

http://act2.me/full-stack-web-development/ 
http://www.sitepoint.com/10-reasons-use-angularjs/ 
http://en.wikipedia.org/wiki/AngularJS

http://www.igvita.com/posa/high-performance-networking-in-google-chrome/ 

--------------------------

Mulțumesc
=========
