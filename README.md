Introducere în AngularJS
========================

![logo](img/AngularJS-large.png)

Radu Potop

--------------------------

AngularJS
=========

A Javascript MVC framework

* two way data binding
* routing
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

* La inceputurile web-ului: give me a doc!

![](img/1.png)

--------------------------

* Server-side apps au evoluat
* Give me a fragment!

![](img/4.png)

--------------------------

* Evolutia pe server-side: Scripts -> Frameworks MVC
* HTML -> JSON
* Folosim tot jQuery

![](img/5.png)

--------------------------

* Am renunțat la Views pe server-side
* Codul pentru a asambla pagini: jQuery -> Javascript MVC Framework

![](img/7.png)

--------------------------

![onward](img/steve-ballmer-shrug.jpg)

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

Model-View-Controller pattern:

* separation of concerns (layers)
* Model = data layer
* View = presentation layer
* Controller = business logic (leaga Model si View)

A lot more than MVC:

* HTML enhanced for web apps
* AngularJS lets you extend HTML vocabulary for your application.


## MVC makes large apps maintainable prin separarea layerelor

--------------------------

Two way data binding
====================

Modificarile din model se propaga instant in view, si invers.

Model <---> View

* Modelul este sincronizat cu View
* Scope = un obiect care leagă Model și View
* Scope are anumite metode: $watch, $get, $set

## Ne scutește de la sincronizarea datelor cu prezentarea și invers

--------------------------

Routing
=======

Încarcă clase/controllere în funcție de link-ul accesat  
Prin hash part al URL-ului

De exemplu ruta `#/campaign/1` va arăta spre controllerul `campaigns(1)` și spre template-ul `campaigns.html`
	
	#/campaign/1 -> campaigns(1){
		...
	};
	

## 

--------------------------

Modules / Servicii
==================

Unitati care incapsuleaza o functionalitate bine definita - **clase**

Servicii
--------

* chart
* pagination
* date picker
* etc.

Many built-in services
----------------------

* xhr, resource, route, location, 

## Contained, reusable code

--------------------------

Dependency Injection
====================

* Serviciile sunt injected in controllere
* Pot fi mocked pentru testare

## Testable, mockable

--------------------------

Directive
=========

* Augmenteaza codul HTML prin elemente sau atribute definite de catre developer.
* Manipularea de DOM se realizeaza in interiorul directivelor
* pentru a nu avea DOM manip in controllere si in tot codul.

Ex:
	
	<input type="text" name="date" date:picker>
	
	
## Less DOM manipulation, DOM manip is contained

--------------------------

Templates
=========

Template

	{{phone.name}}
	
Loops

	<div ng-repeat=”phone in phoneList”>
		{{phone.name}}
	</div>

Filtre
	
	{{15.05 | number}}
	{{'2013-05-13' | date}}
	
etc.

* Declarative is better than procedural

--------------------------

Cum funcționează împreună?
==========================

* aplicația pornește printr-o directivă / un atribut special
* sunt lansate serviciile
* sunt pornite controllerele in functie de ruta curentă
* sunt compilate templates/views care conțin directivele
* se face two way data binding intre modele si views prin intermediul scope


--------------------------

![onward](img/ballmer-ap-photo.jpg)

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

![](img/Ballmer-Tampers-the-Milking-of-Microsoft-Main-Cash-Cow-2.png)
