# README #

This README would normally document whatever steps are necessary to get your application up and running.

## "Tulajdoni hányad" feature adattisztítás ###

### 2017.04.05
* Pythonosítottam néhány ponton a for ciklusokat (x in y az == vizsgálat helyett).
* A darabolós kiértékeléstől (def eval_th_more()) függetlenítettem az írásjelek kitisztítását (def th_replace()), hogy több helyről is lehessen hívni.
* Az adat tisztítást gyorsítottam: a set(string)-el csak az átadott string egyedi jelein halad a for ciklus és vizsgálja meg, hogy az adott írásjel a takarítandó jelek közé tartozik-e. A set miatt csak egyszer.
* Az x/y tulajdoni hányad visszaíráshoz a def th_replace_devider() metódus az első '/' jel jobb oldalán szereplő számot keresi, mint osztót. Ezt tekintjük a hányados osztójának: th_str_div.
* Az x/y tulajdoni hányad osztandóját az 'eval_th' és a 'th_str_div' szorzataként képezzük.
* ---
*

### 2017.03.05
* th_1_per_1 (0/1) feature kreálás
  * th_replace(par1)  : metódus; jel tisztítás
  * eval_th_more(par2): metódus; "1/1" keresés hátulról darabolás és eval(x), str.count(y) használatával









### What is this repository for? ###

* Quick summary
* Version
* [Learn Markdown](https://bitbucket.org/tutorials/markdowndemo)

### How do I get set up? ###

* Summary of set up
* Configuration
* Dependencies
* Database configuration
* How to run tests
* Deployment instructions

### Contribution guidelines ###

* Writing tests
* Code review
* Other guidelines

### Who do I talk to? ###

* Repo owner or admin
* Other community or team contact
