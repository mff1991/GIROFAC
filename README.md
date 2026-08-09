# GIROFAC — Plataforma ERP Web Integral

GIROFAC és una plataforma ERP web orientada a la gestió integral de negoci sota una arquitectura modular i escalable. El projecte s'adopta inicialment sota un entorn de desenvolupament local basat en la pila **LAMP/XAMPP** (Linux/Windows, Apache, MariaDB/MySQL, PHP 8.x), dissenyat amb patrons de desenvolupament desconnectats que garanteixen una transició immediata cap a infraestructures al núvol (VPS, PaaS o entorns contenidoritzats) sense refactorització del codi font.

La interfície es basa en principis **Mobile-First** i disseny adaptatiu (*responsive*), garantint l'accessibilitat des de qualsevol dispositiu i aplicant un control d'accés basat en rols (**RBAC**) que adapta l'experiència d'usuari i la visibilitat dels mòduls en temps real.

---

## Mòduls del Sistema

### 1. Sistema, Configuració i Control d'Accés
* **Configuració Empresarial i Fiscal:** Centralitza dades fiscals, entorns multiidioma (CA, ES, EN), impostos (IVA/IRPF) i sèries de facturació correlativa.
* **Sistema d'Autenticació i Rols (RBAC):** Avalua en temps real la matriu de permisos per habilitar o restringir accions CRUD segons el rol.
* **Registre d'Auditoria i Traçabilitat:** Logging centralitzat per a operacions crítiques (accessos, dades sensibles i transaccions financeres).

### 2. Gestió Comercial i CRM
* **Gestió Unificada de Clients:** Històric fiscal i operatiu per a una visió de 360° de la relació comercial.
* **Cicle de Negociació i Conversió Directa:** Elaboració de pressupostos i conversió automàtica a factura o projecte operatiu.
* **Contractes Recurrents i Subscripcions:** Suport per a facturació periòdica programada.
* **Validació i Signatura Electrònica:** Captura de signatura digital en dispositius mòbils amb registre de traçabilitat (IP, data i hora).

### 3. Operacions, Projectes i Suport Tècnic
* **Planificació i Gestió de Projectes (PM):** Organització en projectes/tasques amb fites temporalitzades i assignació de personal.
* **Control de Temps i Partes d'Hores:** Imputació d'hores facturables i no facturables amb càlcul de rendibilitat en temps real.
* **Gestió d'Incidències i Tiquets:** Suport a clients integrat directament amb els partes d'hores del projecte.
* **Gestió del Coneixement:** Biblioteca tècnica interna per a documentació i procediments.
* **Flux de Facturació per Hores:** Consolidació automàtica d'hores pendents en factures de client (`Client` ➔ `Projecte` ➔ `Partes d'Hores`).

### 4. Comptabilitat i Gestió Financera
* **Facturació Directa i Derivada:** Emissió i recepció de factures complint la normativa fiscal i sèries correlatives.
* **Gestió de Despeses Operatives i de Personal:** Classificació de despeses amb imputació directa a projectes.
* **Conciliació Bancària Automàtica:** Emparellament d'extractes bancaris amb factures pendents i liquidacions.
* **Informes i Registres Fiscals:** Llibres de registre i càlculs preliminars per a liquidacions d'IVA i IRPF.

### 5. Logística, Inventari i Gestió de Proveïdors
* **Gestió de Proveïdors i Catàleg:** Dades de compra, llistes de preus i paràmetres financers (cost vs. PVP) via SKU.
* **Control d'Inventari en Temps Real:** Alertes automàtiques per stock mínim.
* **Automatització de Moviments de Stock:** Descompte i increment automàtic d'unitats segons factures de venda o ordres de compra.

### 6. Recursos Humans, Control Horari i Gestió de Personal
* **Control Horari i Fitxatges:** Registre diari de la jornada (entrades, eixides i pauses) per al compliment laboral.
* **Planificació i Absències:** Gestió de quadrants, torns, vacances i baixes mèdiques.
* **Imputació Cost-Hora i Analítica:** Enllaç del cost/hora empleat amb partes d'hores per determinar el marge real del projecte.

### 7. Màrketing, Comunicació i Agenda Corporativa
* **Màrketing per Correu:** Creació i enviament massiu amb plantilles dinàmiques.
* **Gestió de Màrketing Social:** Planificació editorial mitjançant calendari interactiu.
* **Agenda Unificada:** Cites comercials, fites de projectes i accions de màrketing en una sola interfície.
* **Segmentació Dinàmica:** Filtre d'audiències a partir de les dades del CRM.

---

## Arquitectura Global de Dades i Integració

El valor diferencial de GIROFAC radica en la **interconnexió nativa** de tots els seus mòduls operatius, eliminant els sils d'informació:
1. El cicle de **CRM** transforma opcions d'èxit en projectes (**Operacions**) o factures.
2. L'activitat d'**Operacions** calcula el cost en temps real basant-se en **RRHH** i deriva hores a **Finances**.
3. La compra/venda manté sincronitzats l'**Inventari** i el flux de caixa, finalitzant en la **Conciliació Bancària**.
