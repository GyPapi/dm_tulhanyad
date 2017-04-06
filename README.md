# README #

This README would normally document whatever steps are necessary to get your application up and running.

## "Tulajdoni hányad" feature adattisztítás ###

### 2017.04.06
* def eval_th_more_doubleret(teval_th_more) metódus, amely a tulajdoni hányad értékének és a megbízhatóságának értékpárját adja vissza (érték, minőség) tuple
* ezután a tuple értékpár felhasználásával származtatjuk az új feature-ket


### 2017.04.05
* Pythonosítottam néhány ponton a for ciklusokat (x in y az == vizsgálat helyett). Ismertem, de string változókra nekem eddig nem ment, de most látom, hogy megy.
* A darabolós kiértékeléstől (def eval_th_more()) függetlenítettem az írásjelek kitisztítását (def th_replace()), hogy önállóan is lehessen hívni.
* Az adat tisztítást gyorsítottam: a set(string)-el csak az átadott string egyedi jelein halad a for ciklus és vizsgálja meg, hogy az adott írásjel a takarítandó jelek közé tartozik-e. A set miatt csak egyszer.
* Az x/y tulajdoni hányad visszaíráshoz a def th_replace_devider() metódus az első '/' jel jobb oldalán szereplő számot keresi, mint osztót. Ezt tekintjük a hányados osztójának: th_str_div.
* Az x/y tulajdoni hányad osztandóját az 'eval_th' és a 'th_str_div' szorzataként képezzük: 'th_str_dvd'.
* A  def eval_th_more() metódus visszaadott értékeinek megbízhatósága:
  * sikeres kiértékelés eredményeként float, 
  * sikertelen kiértékelés, de találunk 1/1 kifejezést a stringben, ezért 1.0 float, 
  * sikeres kiértékelés, de az érték > 1.0 float (tapasztalás alapján pl. elmaradt '/' jel/jelek miatt). Ha a string tartalmaz '1/1' jel sorozatot, akkor 1.0 float.
  * minden más esetben None.
*
#### Tervek
* A  df.astype({'th_str_dvd': str,'th_str_div': str})  kifejezéssel az a célom, hogy stringesítsem a két képzett jellemzőt és képezni tudjam az x/y kifejezést.
* A x/y tulajdoni hányadok megbízhatóságára jellemző érték visszadadása.


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
